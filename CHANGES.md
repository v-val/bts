# Changes

## 2024 August 26

* Step containers changed to `while ... ; do ... done`
  for correct handling of step status.
* Fixed problem with failed steps mistakenly handled as successful.
* Fixed problem with logging during BTS completion.
* `bts_untar` updated to extract to directory named as expected (
  doesn't work with `tar` on MacOS).
* Logging respects `${BTS_LOG_LEVEL}` environment variable
* `bts_make` enables overriding command `make` with value of `${BTS_COMMAND_MAKE}` 

## 2024 August 20

* ___Job name___ derived from recipe pathname.
* Log file name changed from `bts.log` to `bts-{job name}.log`.