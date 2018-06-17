gclient_gn_args_file = 'src/build/config/gclient_args.gni'
gclient_gn_args = [
  'build_with_chromium',
  'checkout_android',
  'checkout_android_native_support',
  'checkout_libaom',
  'checkout_nacl',
  'checkout_oculus_sdk',
]


vars = {
  # Variable that can be used to support multiple build scenarios, like having
  # Chromium specific targets in a client project's GN file or sync dependencies
  # conditionally etc.
  'build_with_chromium': True,

  # By default, we should check out everything needed to run on the main
  # chromium waterfalls. This var can be also be set to "small", in order
  # to skip things are not strictly needed to build chromium for development
  # purposes.
  'checkout_configuration': 'default',

  # Pull in Android native toolchain dependencies for Chrome OS too, so we can
  # build ARC++ support libraries.
  'checkout_android_native_support': 'checkout_android or checkout_chromeos',

  # By default, do not check out android sdk sources. This can be overridden
  # e.g. with custom_vars.
  'checkout_android_sdk_sources': False,

  # Check out and download nacl by default. This can be disabled e.g. with
  # custom_vars.
  'checkout_nacl': True,

  # By default, do not check out src-internal. This can be overridden e.g. with
  # custom_vars.
  'checkout_src_internal': False,

  # Fetch the additional packages and files needed to run all of the
  # telemetry tests. This is false by default as some stuff is only
  # privately accessible.
  'checkout_telemetry_dependencies': False,

  # libaom provides support for AV1 but the bitstream is not frozen.
  'checkout_libaom': True,

  # By default do not check out the Oculus SDK. Only available for Googlers.
  'checkout_oculus_sdk' : 'checkout_src_internal and checkout_win',
  'git_url': 'https://chromium.googlesource.com',
}

deps = {
    'src/buildtools':
        Var('git_url') + '/chromium/buildtools.git@5941c1b3df96c1db756a2834343533335c394c4a',
    'src/tools/gyp':
        (Var("git_url")) + '/external/gyp.git@d61a9397e668fa9843c4aa7da9e79460fe590bfb',
}