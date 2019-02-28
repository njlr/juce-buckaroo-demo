load('//:buckaroo_macros.bzl', 'buckaroo_deps')

gcc_pp_flags = [
  '-DJUCE_APP_CONFIG_HEADER="JuceLibraryCode/AppConfig.h"',
]

cxx_binary(
  name = 'app',
  header_namespace = '',
  headers = {
    'JuceLibraryCode/AppConfig.h': 'NetworkGraphicsDemo/JuceLibraryCode/AppConfig.h',
  },
  srcs = glob([
    'NetworkGraphicsDemo/Source/**/*.cpp',
  ]),
  platform_preprocessor_flags = [
    ('linux.*', gcc_pp_flags),
  ],
  deps = buckaroo_deps(),
)
