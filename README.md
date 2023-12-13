# cpp-snippets

## namespace
 Namespace `gh4ck3r` is applied to entire snippets.

## Type
### LazyGetter<GETTER>
 * a type that fetch value from `GETTER()` on first demand.
 * can be assigned with a value prior to `GETTER()`
 * `GETTER` is gone once it has a value by any means.

## Functionality
### hexdump
 Dump linear buffer to `std::string`. Following forms are possible.
  * `hexdump(ptr, len)`: dump from given `ptr` to `len` in byte unit.
  * `hexdump(beg, end)`: dump iterator based range

### concatenate
 Concatenate `constexpr` containers, i.e. std::array, std::string_view.
  * `concat<string_view, string_view, ...>()`: concatenate given `string_view`s
    * Template parameters should have `static` storage class.
    * Concatenated string_view ended with `null`.
  * `concat(std::array...)`: concatenate given `std::array`s
