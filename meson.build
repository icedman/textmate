project('text-edit', 'c', 'cpp',
  version : '0.1',
  default_options : ['warning_level=3', 'cpp_std=c++20']
)

onigmo_files = [
    'libs/Onigmo/regcomp.c',
    'libs/Onigmo/regexec.c',
    'libs/Onigmo/regparse.c',
    'libs/Onigmo/regsyntax.c',
    'libs/Onigmo/st.c',
    'libs/Onigmo/regenc.c',
    'libs/Onigmo/regext.c',
    'libs/Onigmo/regposerr.c',
    'libs/Onigmo/regtrav.c',
    'libs/Onigmo/regerror.c',
    'libs/Onigmo/reggnu.c',
    'libs/Onigmo/regposix.c',
    'libs/Onigmo/regversion.c',
    'libs/Onigmo/enc/ascii.c',
    #'libs/Onigmo/enc/euc_kr.c',
    #'libs/Onigmo/enc/iso_8859_10.c',
    #'libs/Onigmo/enc/iso_8859_16.c',
    #'libs/Onigmo/enc/iso_8859_5.c',
    #'libs/Onigmo/enc/koi8_r.c',
    'libs/Onigmo/enc/us_ascii.c',
    'libs/Onigmo/enc/utf_8.c',
    'libs/Onigmo/enc/windows_1254.c',
    'libs/Onigmo/enc/big5.c',
    'libs/Onigmo/enc/euc_tw.c',
    'libs/Onigmo/enc/iso_8859_11.c',
    'libs/Onigmo/enc/iso_8859_1.c',
    'libs/Onigmo/enc/iso_8859_6.c',
    'libs/Onigmo/enc/koi8_u.c',
    'libs/Onigmo/enc/utf_16be.c',
    #'libs/Onigmo/enc/windows_1250.c',
    #'libs/Onigmo/enc/windows_1257.c',
    #'libs/Onigmo/enc/cp949.c',
    #'libs/Onigmo/enc/gb18030.c',
    'libs/Onigmo/enc/iso_8859_13.c',
    'libs/Onigmo/enc/iso_8859_2.c',
    'libs/Onigmo/enc/iso_8859_7.c',
    #'libs/Onigmo/enc/mktable.c',
    'libs/Onigmo/enc/utf_16le.c',
    #'libs/Onigmo/enc/windows_1251.c',
    #'libs/Onigmo/enc/windows_31j.c',
    #'libs/Onigmo/enc/emacs_mule.c',
    #'libs/Onigmo/enc/gb2312.c',
    'libs/Onigmo/enc/iso_8859_14.c',
    'libs/Onigmo/enc/iso_8859_3.c',
    'libs/Onigmo/enc/iso_8859_8.c',
    'libs/Onigmo/enc/shift_jis.c',
    'libs/Onigmo/enc/utf_32be.c',
    #'libs/Onigmo/enc/windows_1252.c',
    'libs/Onigmo/enc/euc_jp.c',
    #'libs/Onigmo/enc/gbk.c',
    'libs/Onigmo/enc/iso_8859_15.c',
    'libs/Onigmo/enc/iso_8859_4.c',
    'libs/Onigmo/enc/iso_8859_9.c',
    'libs/Onigmo/enc/unicode.c',
    'libs/Onigmo/enc/utf_32le.c'
    #'libs/Onigmo/enc/windows_1253.c'
]

onigmo_includes = [
    'libs/Onigmo',
    'libs/Onigmo/enc',
    'libs/Onigmo/enc/unicode'
]

textmate_inc = include_directories(
    'textmate/parser',
    'textmate/scopes',
    'textmate/theme',
    'textmate/extensions',
    'textmate/data'
)

textmate_files = [
    'textmate/main.cpp',
    'textmate/textmate.cpp',
    'textmate/parser/grammar.cpp',
    'textmate/parser/parser.cpp',
    'textmate/parser/pattern.cpp',
    'textmate/parser/reader.cpp',
    'textmate/scopes/match.cpp',
    'textmate/scopes/parse.cpp',
    'textmate/scopes/scope.cpp',
    'textmate/scopes/types.cpp',
    'textmate/theme/theme.cpp',
    'textmate/extensions/tinyxml2.cpp',
    'textmate/extensions/extension.cpp',
    'textmate/extensions/utf8.cpp',
    'textmate/extensions/util.cpp',
    'textmate/data/themes.cpp',
    'textmate/data/grammars.cpp',
]

jsoncpp_dep = dependency('jsoncpp', required: true)

executable('textmate',
    textmate_files,
    onigmo_files,
    include_directories: [ './', textmate_inc, onigmo_includes ],
    dependencies: [ jsoncpp_dep ],
    install : true
)