# CENTOS-MILAN-SUPPORT-PATCHES

1.	Download kernel-3.10.0-1062.18.1.el7.src.rpm   /   kernel-3.10.0-1160.el7.src.rpm
2.	(  http://vault.centos.org/centos/7/os/Source/SPackages   http://vault.centos.org/centos/7/updates/Source/SPackages    https://buildlogs.centos.org/c7.1908.u.x86_64/kernel/20200317234648/3.10.0-1062.18.1.el7.x86_64/kernel-3.10.0-1062.18.1.el7.src.rpm )	
4.	Get   (from 'rpm' above)   linux-3.10.0-1062.18.1.el7.tar.xz     /   linux-3.10.0-1160.el7.tar.xz
5.	Apply Milan Backported Patches: 
6.	         0001-edac-mce-milan.patch,  0002-milan-support.patch,  0003-events-milan.patch,  0004-kernel-milan.patch,  0005-support-milan.patch,  0006-kvm-milan.patch
                                    
4.	Please apply each patch sequentially:         patch -p1 < {0001...0006 .patch}
5.	Or each Patch sequentially, using git am:     git am {0001...0006 .patch}
6.	Or each Patch sequentially, using git apply:  git apply {0001...0006 .patch}

7.	Please use - kernel-3.10.0-x86_64.config or kernel-3.10.0-x86_64-debug.config for building kernel.
8.	Build, Install patched kernel:  make all, make modules_install, make install
