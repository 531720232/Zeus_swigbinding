# Zeus_swigbinding
Zeus 下swig绑定文件部分
%module(directors="1") Zeus_Ne

%feature("director");

%include <std_string.i>
%include "cpointer.i"
%{

#include "imgui.h"
#include "imgui_internal.h"
%}

/* Parse the header file to generate wrappers */
%include "imgui.h"
%include "imgui_internal.h"
//%pointer_functions(bool, boolp); 
%pointer_class(bool, swbool);
//func 调用static,一步到位，类似于c，class比较麻烦，还要cast
