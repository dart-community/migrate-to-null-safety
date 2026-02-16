# Null safety example: A CLI app for calculating lix

> [!NOTE]
> **This is an archived sample.**
> It was originally published in the
> [dart-lang/samples](https://github.com/dart-lang/samples) repository.
>
> It might contain outdated dependencies or practices.
> For current Dart samples, check out the
> [Dart samples repository](https://github.com/dart-lang/samples).

This is a small code example of an app that calculates the
'lix' readability index for a text file.
The implementation relies on Dart's support for null safety and is
meant to demonstrate some of the related features in a practical example.

## Supported SDK versions

Running the example requires Dart 2.12 or later.
If you're using Flutter, you need Flutter 2.0 or later.

### Running from the terminal / command prompt

To run the main app, run the following command
from the root of the `calculate_lix` directory:

```bash
dart run bin/main.dart text/lorem-ipsum.txt
```

## Next steps

Once you have the code running, here are some things you can try:

* In `lib/lix.dart` on line 31, try to
  remove the `required` keyword from
  one or more parameters in the constructor,
  and notice the error shown.

* In `lib/lix.dart` on line 47, try to
  delete the code that initializes one or more fields (such as `words: words`)
  and notice the error shown.

* In `lib/lix.dart` on line 9, try to
  make `words` a nullable variable (by changing `int` to `int?`).
  Then notice how the analyzer reports errors in the `_calculate` method due to
  trying to unconditionally divide with a value that's potentially `null`.

* In `lib/lix.dart` on line 22, try to
  remove the `late` keyword from `readability`, and notice how
  the analyzer reports an error in the constructor.
