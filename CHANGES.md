# Changes
## 2024 November 19
A bunch of changes:
* Name of file indicating success of `bts_step` changed to
  lowercased dependency name with ".bts" prefix. E.g.: `.bts.mold`
* Downloaded files and build directories removed
  upon successful completion of step and entire job.
* Each `bts_get` invocation downloads and extracts to separate directory,
  named after BTS_STEP_TAG and downloaded file.
* BTS_BUILD_DIR sets common prefix to build directories.  
  By default build directory created next to source directory 
  with same name but ".build" suffix.
* BTS_WORK_DIR enables customization of `bts` working directory.  
  By default it is ".bts" in target directory. 
## 2024 August 20
* ___Job name___ derived from recipe pathname.
* Log file name changed from `bts.log` to `bts-{job name}.log`.