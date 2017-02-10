My first Hello World JNI in Windows.

NOTE: Used DevC++ migwin for gcc compiler

Following commands to be run from cmd prompt
-- javac HelloJNI.java
-- javah HelloJNI
>>gcc -c -I"C:\Program Files\Java\jdk1.8.0_101\include" -I"C:\Program Files\Java\jdk1.8.0_101\include\win32" "HelloJNI.cpp"
>>gcc -Wl,--add-stdcall-alias -m64 -shared -o hello.dll HelloJNI.o
>>java HelloJNI
