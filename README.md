## Usage

```
composer require --dev
```

Then write a `.phpcs.xml.dist` file:

```xml
<?xml version="1.0"?>
<ruleset>
    <arg name="basepath" value="."/>

    <file>src</file>
    <file>tests</file>

    <rule ref="HardMode"/>
</ruleset>
```

Then run the analysis:

```
vendor/bin/phpcs
```

Or using [pretty](https://github.com/mnapoli/pretty):

```
vendor/bin/pretty
```

## Fixing errors

Run:

```
vendor/bin/phpcbf
```

Or using [pretty](https://github.com/mnapoli/pretty):

```
vendor/bin/pretty fix
```

## Advanced configuration

Check out the [PHP CodeSniffer documentation](https://github.com/squizlabs/PHP_CodeSniffer/wiki) for all the options. You will find below documentation for common scenarios.

To exclude some files from the analysis:

```xml
<exclude-pattern>tests/Fixtures</exclude-pattern>
```

On large projects you may want to use PHP CodeSniffer's cache:

```xml
<arg name="cache" value=".phpcs-cache"/>
```

Remember to add `.phpcs-cache` to `.gitignore`.
