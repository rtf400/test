# test
# aa:
   - 
   - 
# How to use:

1. aaa

   >> aaa
  
   aaa:
   
2. bb

   >> bb
   
   bbb: 
     - cc

   Vlfeat:
     - >> cd lib/vlfeat/ && make
     - cd ./toolbox in Matlab editor.
     - Run vl_setup
     - Compile mex Hog functions:
       >> cd misc
       >> mex -L../../bin/glnx86 -lvl -I../ -I../../ vl_hog.c
     - Setup libvl.so path.
     - Assume that your libvl.so located at: <vlfeat_folder>/bin/glnx86
       Create soft link:
       >> ln -s <vlfeat_folder>/bin/glnx86/libvl.so /usr/local/libvl.so
       Check if the libvl.so is ready to use.
       >> ldd vl_hog.mexglx
       If libvl.so still not found.
       Add /usr/local/lib into /etc/ld.so.conf (sudo).
       >> sudo ldconfig
       >> ldconfig -p | grep libvl.so
       Check again: >> ldd vl_hog.mexglx
      

3. If you run first time. You should set these following parameters
   to learn shape and variation. For later time, reset to 0.

   options.learningShape     = 1;
   options.learningVariation = 1;

4. Do training:
   >> run_training();
   
5. Do testing:
   >> do_testing();


Note: in the program, we provide training models of LFPW (68 landmarks) in folder:
"./model". The program does not optimize speed and memory during training, the 
memory problem may happens if you train on too much data.
