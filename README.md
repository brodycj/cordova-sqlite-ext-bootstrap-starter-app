# Cordova sqlite ext pre-populated database bootstrap starter

**AUTHOR:** [@brodybits (Christopher J. Brody aka Chris Brody)](https://github.com/brodybits)

**LICENSE:** [CC0 1.0 (public domain)](https://creativecommons.org/publicdomain/zero/1.0/)

**NOTE:** This project includes JQuery (3.3.1) and Bootstrap 3 (3.3.7) under the MIT license. Otherwise there is no code copied from other sources.

**IMPORTANT:** Whitelist and intent items are omitted from this test app.

## Dependencies

- Bootstrap (3.3.7) - included (MIT license)
- JQuery (3.3.1) - included (MIT license)
- `cordova-plugin-dialogs` - specified in `config.xml`
- `cordova-sqlite-ext` - specified in `config.xml`

_IMPORTANT NOTE: `cordova-plugin-dialogs` and `cordova-sqlite-ext` were added using the `--save` flag to ensure that these plugins would be automatically installed. It is recommended to use the `--save` flags to add any other plugins rather than adding such plugins to git (this is automatic starting with Cordova `7.0`)._

Additional note: `cordova-plugin-dialogs` does not currently support macOS ("osx"). As a workaround this project automatically uses `window.alert` if necessary.

## How to run

1. Add the desired platform(s), for example:

```shell
cordova platform add android
```

2. Do `cordova prepare` (not always be necessary but good to be on the safe side):

```shell
cordova prepare
```

3. Run it on your mobile emulator or device, for example:

```shell
cordova run android
```

## Functionality

- Upon startup: open the pre-popualted database with 3 records
- Alert dialog test (native alert if possible)
- Echo test
- Self test
- Location reload
- String test 1
- String test 2 (string as a SQL parameter)
- Show first record
- Show record count
- Add record
- Add 100 records from JavaScript object after delay
- Delete all records
- Follow link to page 2
- Change window.location to page 2

## Multi-page test

It is possible to switch between two pages using "follow link" buttons. The main page also has a button to go to page 2 by changing `window.location`. There is also a button on both pages to try `location.reload()`.

The sqlite plugin should continue to work after the user changes to another page or triggers `location.reload()`.
