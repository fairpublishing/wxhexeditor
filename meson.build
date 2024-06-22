project('wxHexEditor', 'cpp',
  version : '0.24',
  default_options : ['warning_level=3', 'cpp_std=c++14'])

wxwidgets_dep = dependency('wxwidgets', modules: ['base', 'core', 'aui', 'xml', 'net'])
mhash_dep     = dependency('mhash')
udis86_dep    = dependency('udis86')

# Normally we should not have zlib as an explicit dependency but when wxwidgets is used
# as a static library it does not list zlib in the output from wx-config --libs
zlib_dep      = dependency('zlib')

# Source files
src_files = [
  'src/HexEditorGui.cpp',
  'src/FAL.cpp',
  'src/HexDialogs.cpp',
  'src/HexPanels.cpp',
  'src/HexEditorApp.cpp',
  'src/HexEditor.cpp',
  'src/HexEditorCtrl/HexEditorCtrl.cpp',
  'src/HexEditorCtrl/wxHexCtrl/TagDialogGui.cpp',
  'src/HexEditorCtrl/wxHexCtrl/wxHexCtrl.cpp',
  'src/HexEditorCtrl/wxHexCtrl/Tag.cpp',
  'src/HexEditorCtrl/HexEditorCtrlGui.cpp',
  'src/HexEditorFrame.cpp'
]

executable('wxHexEditor',
  sources : src_files,
  dependencies : [wxwidgets_dep, mhash_dep, udis86_dep, zlib_dep],
  install : true)
