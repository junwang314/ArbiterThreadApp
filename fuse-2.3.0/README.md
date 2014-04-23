Compile with Arbiter
===================

* make changes to configure.in:
+CPPFLAGS="$CPPFLAGS -I$AB_ROOT/common/include -I$LIB_CLIENT"

* make changes to lib/Makefile.am:
-   fuse_kernel_compat5.h
+   fuse_kernel_compat5.h \
+   $(AB_ROOT)/client_module/lib_client.c

* autoreconf --install

* ./configure

* make
