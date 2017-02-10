My first Hello World JNI in Windows.</br>

NOTE: Used DevC++ migwin for gcc compiler</br>

Following commands to be run from cmd prompt </br>
javac HelloJNI.java </br>
javah HelloJNI</br>
gcc -c -I"C:\Program Files\Java\jdk1.8.0_101\include" -I"C:\Program Files\Java\jdk1.8.0_101\include\win32" "HelloJNI.cpp"</br>
gcc -Wl,--add-stdcall-alias -m64 -shared -o hello.dll HelloJNI.o</br>
java HelloJNI</br>
