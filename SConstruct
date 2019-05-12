#!/usr/bin/env python3

#Local
import methods

env=Environment(CPPPATH=['#modules'],CXXFLAGS="-std=c++17")

env.__class__.add_source_files = methods.add_source_files
env.__class__.add_library = methods.add_library

Export('env')

#0 is the obj_list
#1 is the src_list for formatting
#2 is the hdr_list for formatting
SConscript('core/SConscript')
SConscript('modules/SConscript')

env.Program('devoured', 'main.cpp')
