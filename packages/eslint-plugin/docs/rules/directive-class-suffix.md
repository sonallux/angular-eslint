<!--

  DO NOT EDIT.

  This markdown file was autogenerated using a mixture of the following files as the source of truth for its data:
  - ../../src/rules/directive-class-suffix.ts
  - ../../tests/rules/directive-class-suffix/cases.ts

  In order to update this file, it is therefore those files which need to be updated, as well as potentially the generator script:
  - ../../../../tools/scripts/generate-rule-docs.ts

-->

<br>

# `@angular-eslint/directive-class-suffix`

Classes decorated with @Directive must have suffix "Directive" (or custom) in their name. See more at https://angular.io/styleguide#style-02-03

- Type: suggestion
- Category: Best Practices

<br>

## Rule Options

The rule accepts an options object with the following properties:

```ts
interface Options {
  /**
   * Default: `["Directive"]`
   */
  suffixes?: string[];
}

```

<br>

## Usage Examples

> The following examples are generated automatically from the actual unit tests within the plugin, so you can be assured that their behavior is accurate based on the current commit.

<br>

<details>
<summary>❌ - Toggle examples of <strong>incorrect</strong> code for this rule</summary>

<br>

#### Default Config

```json
{
  "rules": {
    "@angular-eslint/directive-class-suffix": [
      "error"
    ]
  }
}
```

<br>

#### ❌ Invalid Code

```ts
@Directive({
  selector: 'sg-foo-bar'
})
class Test {}
      ~~~~
```

<br>

---

<br>

#### Default Config

```json
{
  "rules": {
    "@angular-eslint/directive-class-suffix": [
      "error"
    ]
  }
}
```

<br>

#### ❌ Invalid Code

```ts
@Directive({
  selector: 'sg-foo-bar'
})
class TestDirectivePage implements AsyncValidator {}
      ~~~~~~~~~~~~~~~~~
```

<br>

---

<br>

#### Custom Config

```json
{
  "rules": {
    "@angular-eslint/directive-class-suffix": [
      "error",
      {
        "suffixes": [
          "Page"
        ]
      }
    ]
  }
}
```

<br>

#### ❌ Invalid Code

```ts
@Directive({
  selector: 'sgBarFoo'
})
class TestPageDirective {}
      ~~~~~~~~~~~~~~~~~
```

</details>

<br>

---

<br>

<details>
<summary>✅ - Toggle examples of <strong>correct</strong> code for this rule</summary>

<br>

#### Default Config

```json
{
  "rules": {
    "@angular-eslint/directive-class-suffix": [
      "error"
    ]
  }
}
```

<br>

#### ✅ Valid Code

```ts
@Directive({
  selector: 'sgBarFoo'
})
class TestDirective {}
```

<br>

---

<br>

#### Default Config

```json
{
  "rules": {
    "@angular-eslint/directive-class-suffix": [
      "error"
    ]
  }
}
```

<br>

#### ✅ Valid Code

```ts
@Directive({
  selector: 'sgBarFoo'
})
class TestValidator implements Validator {}
```

<br>

---

<br>

#### Default Config

```json
{
  "rules": {
    "@angular-eslint/directive-class-suffix": [
      "error"
    ]
  }
}
```

<br>

#### ✅ Valid Code

```ts
@Directive({
  selector: 'sgBarFoo'
})
class TestValidator implements AsyncValidator {}
```

<br>

---

<br>

#### Default Config

```json
{
  "rules": {
    "@angular-eslint/directive-class-suffix": [
      "error"
    ]
  }
}
```

<br>

#### ✅ Valid Code

```ts
@Directive
class Test {}
```

<br>

---

<br>

#### Default Config

```json
{
  "rules": {
    "@angular-eslint/directive-class-suffix": [
      "error"
    ]
  }
}
```

<br>

#### ✅ Valid Code

```ts
@Directive()
class Test {}
```

<br>

---

<br>

#### Default Config

```json
{
  "rules": {
    "@angular-eslint/directive-class-suffix": [
      "error"
    ]
  }
}
```

<br>

#### ✅ Valid Code

```ts
@Component({
  selector: 'sg-bar-foo'
})
class TestComponent {}
```

<br>

---

<br>

#### Default Config

```json
{
  "rules": {
    "@angular-eslint/directive-class-suffix": [
      "error"
    ]
  }
}
```

<br>

#### ✅ Valid Code

```ts
@Pipe({
  name: 'sgPipe'
})
class TestPipe {}
```

<br>

---

<br>

#### Default Config

```json
{
  "rules": {
    "@angular-eslint/directive-class-suffix": [
      "error"
    ]
  }
}
```

<br>

#### ✅ Valid Code

```ts
@Injectable()
class TestService {}
```

<br>

---

<br>

#### Default Config

```json
{
  "rules": {
    "@angular-eslint/directive-class-suffix": [
      "error"
    ]
  }
}
```

<br>

#### ✅ Valid Code

```ts
class TestEmpty {}
```

<br>

---

<br>

#### Custom Config

```json
{
  "rules": {
    "@angular-eslint/directive-class-suffix": [
      "error",
      {
        "suffixes": [
          "Dir"
        ]
      }
    ]
  }
}
```

<br>

#### ✅ Valid Code

```ts
@Directive({
  selector: 'sgBarFoo'
})
class TestDir {}
```

<br>

---

<br>

#### Custom Config

```json
{
  "rules": {
    "@angular-eslint/directive-class-suffix": [
      "error",
      {
        "suffixes": [
          "Page",
          "View"
        ]
      }
    ]
  }
}
```

<br>

#### ✅ Valid Code

```ts
@Directive({
  selector: 'sgBarFoo'
})
class TestPage {}
```

</details>

<br>