# Modify Numpy Library Log base 10 to base 9

##About:
This repo is cloned from https://github.com/numpy/numpy and then I have added a log base 9 functionality  in core numpy.

I have created a git branch from master named “numpy/log9”

## Dev Env : 

I have build it on Linux(ubuntu) with gcc and Fortran77  binaries and other math core lib. 
I have used virtual env for this. 

Details:
https://www.numpy.org/devdocs/user/building.html 
https://docs.scipy.org/doc/numpy/dev/style_guide.html#function-documentation

## Git Checkout

git checkout branch numpy/log9

'''
Commit message for specific file change:
numpy/core/code_generators/generate_umath.py
	generative function for log base 9 in generate_umath
numpy/core/include/numpy/npy_math.h
	Adding constant and converter function in math header
numpy/core/src/umath/funcs.inc.src
	Adding static func in core src for c
numpy/core/umath.py
	exposing log9 via umath.py
numpy/lib/scimath.py
	scimath log9 is just utility built over logn 
numpy/ma/core.py
	in core math masking log9 from umath core
'''
## Build Numpy

python setup.py build 

