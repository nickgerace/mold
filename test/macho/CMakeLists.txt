set(MOLD_MACHO_TESTS
  U
  Z
  add-ast-path
  add-empty-section
  adhoc-codesign
  all-load
  application-extension
  archive
  baserel
  basic
  bss
  bundle
  comdat
  common
  common-alignment
  cstring
  data-reloc
  dead-strip
  dead-strip-dylibs
  dead-strip-dylibs2
  dependency-info
  dlinfo
  duplicate-error
  dylib
  entry
  exception
  export-dynamic
  exported-symbols-list
  filepath
  filepath2
  force-load
  framework
  headerpad
  headerpad-max-install-names
  hello
  hello2
  hello3
  hello4
  hello5
  hidden-l
  install-name
  lc-build-version
  lc-linker-option
  lib1
  libunwind
  linker-optimization-hints
  lto
  lto-dead-strip-dylibs
  macos-version-min
  map
  merge-scope
  missing-error
  needed-framework
  needed-l
  no-function-starts
  objc
  objc-selector
  object-path-lto
  order-file
  pagezero-size
  pagezero-size2
  pagezero-size3
  platform-version
  private-extern
  reexport-l
  reproducibility
  response-file
  rpath
  search-dylibs-first
  search-paths-first
  sectcreate
  stack-size
  start-stop-symbol
  subsections-via-symbols
  syslibroot
  tbd
  tbd-add
  tbd-hide
  tbd-install-name
  tbd-previous
  tbd-reexport
  tls
  tls2
  undef
  unexported-symbols-list
  universal
  unkown-tbd-target
  uuid
  uuid2
  weak-def
  weak-def-dylib
  weak-def-ref
  weak-l
  weak-undef
  )

foreach(TEST IN LISTS MOLD_MACHO_TESTS)
  add_test(NAME ${TEST}
    COMMAND bash -x ${CMAKE_CURRENT_LIST_DIR}/${TEST}.sh
    WORKING_DIRECTORY ${mold_BINARY_DIR})
endforeach()
