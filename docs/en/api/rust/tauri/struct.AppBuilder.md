---
title: "struct.AppBuilder"
---

# Struct [tauri](/docs/api/rust/tauri/index.html)::​[AppBuilder](/docs/api/rust/tauri/)

    pub struct AppBuilder { /* fields omitted */ }

The App builder.

## Implementations

### `impl AppBuilder`

#### `pub fn new() -> Self`

Creates a new App builder.

#### `pub fn invoke_handler<F: FnMut(&mut Webview<'_>, &str) -> Result<(), String> + 'static>( self, invoke_handler: F ) -> Self`

Defines the JS message handler callback.

#### `pub fn setup<F: FnMut(&mut Webview<'_>, String) + 'static>( self, setup: F ) -> Self`

Defines the setup callback.

#### `pub fn splashscreen_html(self, html: &str) -> Self`

Defines the splashscreen HTML to render.

#### `pub fn plugin(self, plugin: impl Plugin + 'static) -> Self`

Adds a plugin to the runtime.

#### `pub fn build(self) -> App`

Builds the App.

## Trait Implementations

### `impl Default for AppBuilder`

#### `fn default() -> AppBuilder`

Returns the "default value" for a type. [Read more](https://doc.rust-lang.org/nightly/core/default/trait.Default.html#tymethod.default)

## Auto Trait Implementations

### `impl !RefUnwindSafe for AppBuilder`

### `impl !Send for AppBuilder`

### `impl !Sync for AppBuilder`

### `impl Unpin for AppBuilder`

### `impl !UnwindSafe for AppBuilder`

## Blanket Implementations

### `impl<T> Any for T where T: 'static + ?Sized,`

#### `fn type_id(&self) -> TypeId`

Gets the `TypeId` of `self`. [Read more](https://doc.rust-lang.org/nightly/core/any/trait.Any.html#tymethod.type_id)

### `impl<T> Borrow<T> for T where T: ?Sized,`

#### `fn borrow(&self) -> &T`

Immutably borrows from an owned value. [Read more](https://doc.rust-lang.org/nightly/core/borrow/trait.Borrow.html#tymethod.borrow)

### `impl<T> BorrowMut<T> for T where T: ?Sized,`

#### `fn borrow_mut(&mut self) -> &mutT`

Mutably borrows from an owned value. [Read more](https://doc.rust-lang.org/nightly/core/borrow/trait.BorrowMut.html#tymethod.borrow_mut)

### `impl<T> From<T> for T`

#### `fn from(t: T) -> T`

Performs the conversion.

### `impl<T, U> Into<U> for T where U: From<T>,`

#### `fn into(self) -> U`

Performs the conversion.

### `impl<T> Pointable for T`

#### `const ALIGN: usize`

The alignment of pointer.

#### `type Init = T`

The type for initializers.

#### `unsafe fn init(init: <T as Pointable>::Init) -> usize`

Initializes a with the given initializer. [Read more](/docs/api/rust/tauri/about:blank#tymethod.init)

#### `unsafe fn deref<'a>(ptr: usize) -> &'aT`

Dereferences the given pointer. [Read more](/docs/api/rust/tauri/about:blank#tymethod.deref)

#### `unsafe fn deref_mut<'a>(ptr: usize) -> &'a mutT`

Mutably dereferences the given pointer. [Read more](/docs/api/rust/tauri/about:blank#tymethod.deref_mut)

#### `unsafe fn drop(ptr: usize)`

Drops the object pointed to by the given pointer. [Read more](/docs/api/rust/tauri/about:blank#tymethod.drop)

### `impl<T, U> TryFrom<U> for T where U: Into<T>,`

#### `type Error = Infallible`

The type returned in the event of a conversion error.

#### `fn try_from(value: U) -> Result<T, <T as TryFrom<U>>::Error>`

Performs the conversion.

### `impl<T, U> TryInto<U> for T where U: TryFrom<T>,`

#### `type Error = <U as TryFrom<T>>::Error`

The type returned in the event of a conversion error.

#### `fn try_into(self) -> Result<U, <U as TryFrom<T>>::Error>`

Performs the conversion.

### `impl<V, T> VZip<V> for T where V: MultiLane<T>,`

#### `fn vzip(self) -> V`
