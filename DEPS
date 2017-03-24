vars = {
    'git_url': 'https://chromium.googlesource.com',
}

deps = {
    'src/buildtools':
        Var('git_url') + '/chromium/buildtools.git@39b1db2ab4aa4b2ccaa263c29bdf63e7c1ee28aa',
}

hooks = [{
    'action': [
        'download_from_google_storage',
        '--no_resume',
        '--platform=win32',
        '--no_auth',
        '--bucket',
        'chromium-gn',
        '-s',
        'src/buildtools/win/gn.exe.sha1'
    ],
    'pattern': '.',
    'name': 'gn_win'
}, {
    'action': [
        'download_from_google_storage',
        '--no_resume',
        '--platform=darwin',
        '--no_auth',
        '--bucket',
        'chromium-gn',
        '-s',
        'src/buildtools/mac/gn.sha1'
    ],
    'pattern': '.',
    'name': 'gn_mac'
}, {
    'action': [
        'download_from_google_storage',
        '--no_resume',
        '--platform=linux*',
        '--no_auth',
        '--bucket',
        'chromium-gn',
        '-s',
        'src/buildtools/linux32/gn.sha1'
    ],
    'pattern': '.',
    'name': 'gn_linux32'
}, {
    'action': [
        'download_from_google_storage',
        '--no_resume',
        '--platform=linux*',
        '--no_auth',
        '--bucket',
        'chromium-gn',
        '-s',
        'src/buildtools/linux64/gn.sha1'
    ],
    'pattern': '.',
    'name': 'gn_linux64'
}, {
    'action': [
      'python',
      'src/build/vs_toolchain.py',
      'update'
    ],
    'pattern':
      '.',
    'name':
      'win_toolchain'
  }]
