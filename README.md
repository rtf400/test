# test
# aa:
   - 
   - 
# aaa:

1. aaa

   >> aaa
  
   aaa:
   
2. bb

   >> bb
   
   bbb: 
     - cc

   ddd:
     - ddd:
       >> ln -s <vlfeat_folder>/bin/glnx86/libvl.so /usr/local/libvl.so
       Check if the libvl.so is ready to use.
       >> ldd vl_hog.mexglx
       If libvl.so still not found.
       Add /usr/local/lib into /etc/ld.so.conf (sudo).
       >> sudo ldconfig
       >> ldconfig -p | grep libvl.so
       Check again: >> ldd vl_hog.mexglx
      
3. ee:
   >> ee
   
4. ff
   >> ff


Note: blabla
