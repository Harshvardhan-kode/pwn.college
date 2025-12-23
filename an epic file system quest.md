# Linux Luminarium

## Module 3:comprehending commands  

### Challenge: an epic file system quest

**Commands Used:**
```bash
hacker@commands~an-epic-filesystem-quest:~$ cd /
hacker@commands~an-epic-filesystem-quest:/$ ls
INSIGHT  boot       dev  flag  lib    lib64   media  nix  proc  run   srv  tmp  var
bin      challenge  etc  home  lib32  libx32  mnt    opt  root  sbin  sys  usr
hacker@commands~an-epic-filesystem-quest:/$ cat flag
cat: flag: Permission denied
hacker@commands~an-epic-filesystem-quest:/$ cd flag
bash: cd: flag: Not a directory
hacker@commands~an-epic-filesystem-quest:/$ cat /flag
cat: /flag: Permission denied
hacker@commands~an-epic-filesystem-quest:/$ cat ./flag
cat: ./flag: Permission denied
hacker@commands~an-epic-filesystem-quest:/$ cat INSIGHT 
Great sleuthing!
The next clue is in: /usr/share/emacs/26.3/site-lisp
hacker@commands~an-epic-filesystem-quest:/$ cd /usr/share/emacs/26.3/site-lisp
hacker@commands~an-epic-filesystem-quest:/usr/share/emacs/26.3/site-lisp$ ls
SECRET  subdirs.el
hacker@commands~an-epic-filesystem-quest:/usr/share/emacs/26.3/site-lisp$ cat SECRET 
Yahaha, you found me!
The next clue is in: /usr/local/lib/python3.8/dist-packages/IPython/core/profile

The next clue is **hidden** --- its filename starts with a '.' character. You'll need to look for it using special options to 'ls'.
hacker@commands~an-epic-filesystem-quest:/usr/share/emacs/26.3/site-lisp$ cat /usr/local/lib/python3.8/dist-packages/IPython/core/pro
profile/       profileapp.py  profiledir.py  prompts.py     
hacker@commands~an-epic-filesystem-quest:/usr/share/emacs/26.3/site-lisp$ cat /usr/local/lib/python3.8/dist-packages/IPython/core/profile
cat: /usr/local/lib/python3.8/dist-packages/IPython/core/profile: Is a directory
hacker@commands~an-epic-filesystem-quest:/usr/share/emacs/26.3/site-lisp$ cd /usr/local/lib/python3.8/dist-packages/IPython/core/profile
hacker@commands~an-epic-filesystem-quest:/usr/local/lib/python3.8/dist-packages/IPython/core/profile$ ls
README_STARTUP
hacker@commands~an-epic-filesystem-quest:/usr/local/lib/python3.8/dist-packages/IPython/core/profile$ cat README_STARTUP 
This is the IPython startup directory

.py and .ipy files in this directory will be run *prior* to any code or files specified
via the exec_lines or exec_files configurables whenever you load this profile.

Files will be run in lexicographical order, so you can control the execution order of files
with a prefix, e.g.::

    00-first.py
    50-middle.py
    99-last.ipy
hacker@commands~an-epic-filesystem-quest:/usr/local/lib/python3.8/dist-packages/IPython/core/profile$ first.py
bash: first.py: command not found
hacker@commands~an-epic-filesystem-quest:/usr/local/lib/python3.8/dist-packages/IPython/core/profile$ cat first.py
cat: first.py: No such file or directory
hacker@commands~an-epic-filesystem-quest:/usr/local/lib/python3.8/dist-packages/IPython/core/profile$ ls
README_STARTUP
hacker@commands~an-epic-filesystem-quest:/usr/local/lib/python3.8/dist-packages/IPython/core/profile$ ls -a
.  ..  .GIST  README_STARTUP
hacker@commands~an-epic-filesystem-quest:/usr/local/lib/python3.8/dist-packages/IPython/core/profile$ cat .GIST 
Lucky listing!
The next clue is in: /opt/busybox/busybox-1.33.2/shell/ash_test/ash-read
hacker@commands~an-epic-filesystem-quest:/usr/local/lib/python3.8/dist-packages/IPython/core/profile$ cd /opt/busybox/busybox-1.33.2/shell/ash_test/ash-read
hacker@commands~an-epic-filesystem-quest:/opt/busybox/busybox-1.33.2/shell/ash_test/ash-read$ ls
README            read_SIGCHLD.right  read_d0.tests   read_n.right  read_r.tests  read_t0.right
read_REPLY.right  read_SIGCHLD.tests  read_ifs.right  read_n.tests  read_t.right  read_t0.tests
read_REPLY.tests  read_d0.right       read_ifs.tests  read_r.right  read_t.tests
hacker@commands~an-epic-filesystem-quest:/opt/busybox/busybox-1.33.2/shell/ash_test/ash-read$ cat README 
Tubular find!
The next clue is in: /usr/share/racket/pkgs/htdp-lib/htdp/bsl/lang/compiled

The next clue is **delayed** --- it will not become readable until you enter the directory with 'cd'.
hacker@commands~an-epic-filesystem-quest:/opt/busybox/busybox-1.33.2/shell/ash_test/ash-read$ cd /usr/share/racket/pkgs/htdp-lib/htdp/bsl/lang/compiled
hacker@commands~an-epic-filesystem-quest:/usr/share/racket/pkgs/htdp-lib/htdp/bsl/lang/compiled$ ls
TEASER  reader_rkt.dep  reader_rkt.zo
hacker@commands~an-epic-filesystem-quest:/usr/share/racket/pkgs/htdp-lib/htdp/bsl/lang/compiled$ cat TEASER 
Congratulations, you found the clue!
The next clue is in: /opt/linux/linux-5.4/include/uapi/linux/spi

The next clue is **delayed** --- it will not become readable until you enter the directory with 'cd'.
hacker@commands~an-epic-filesystem-quest:/usr/share/racket/pkgs/htdp-lib/htdp/bsl/lang/compiled$ cd /opt/linux/linux-5.4/include/uapi/linux/spi
hacker@commands~an-epic-filesystem-quest:/opt/linux/linux-5.4/include/uapi/linux/spi$ ls
TIP  spidev.h
hacker@commands~an-epic-filesystem-quest:/opt/linux/linux-5.4/include/uapi/linux/spi$ cat TIP
Great sleuthing!
The next clue is in: /usr/share/doc/shared-mime-info/shared-mime-info-spec.html

Watch out! The next clue is **trapped**. You'll need to read it out without 'cd'ing into the directory; otherwise, the clue will self destruct!
hacker@commands~an-epic-filesystem-quest:/opt/linux/linux-5.4/include/uapi/linux/spi$ cat /usr/s
sbin/  share/ src/   
hacker@commands~an-epic-filesystem-quest:/opt/linux/linux-5.4/include/uapi/linux/spi$ cat /usr/share/doc/shared-mime-info/shared-mime-info-spec.html
cat: /usr/share/doc/shared-mime-info/shared-mime-info-spec.html: Is a directory
hacker@commands~an-epic-filesystem-quest:/opt/linux/linux-5.4/include/uapi/linux/spi$ ls /usr/share/doc/shared-mime-info/shared-mime-info-spec.htm
l
BRIEF-TRAPPED  b518.html  index.html  x34.html  x497.html
hacker@commands~an-epic-filesystem-quest:/opt/linux/linux-5.4/include/uapi/linux/spi$ cat BRIEF-TRAPPED
cat: BRIEF-TRAPPED: No such file or directory
hacker@commands~an-epic-filesystem-quest:/opt/linux/linux-5.4/include/uapi/linux/spi$ ls -a /usr/share/doc/shared-mime-info/shared-mime-info-spec.
html
.  ..  BRIEF-TRAPPED  b518.html  index.html  x34.html  x497.html
hacker@commands~an-epic-filesystem-quest:/opt/linux/linux-5.4/include/uapi/linux/spi$ cat /usr/share/doc/shared-mime-info/shared-mime-info-spec.html/BRIEF-TRAPPED 
Yahaha, you found me!
The next clue is in: /opt/linux/linux-5.4/drivers/gpu/drm/mediatek
hacker@commands~an-epic-filesystem-quest:/opt/linux/linux-5.4/include/uapi/linux/spi$ cd /opt/linux/linux-5.4/drivers/gpu/drm/mediatek
hacker@commands~an-epic-filesystem-quest:/opt/linux/linux-5.4/drivers/gpu/drm/mediatek$ ls
EVIDENCE   mtk_disp_color.c  mtk_drm_crtc.c      mtk_drm_ddp_comp.h  mtk_drm_gem.c    mtk_hdmi.c      mtk_hdmi_regs.h
Kconfig    mtk_disp_ovl.c    mtk_drm_crtc.h      mtk_drm_drv.c       mtk_drm_gem.h    mtk_hdmi.h      mtk_mipi_tx.c
Makefile   mtk_disp_rdma.c   mtk_drm_ddp.c       mtk_drm_drv.h       mtk_drm_plane.c  mtk_hdmi_ddc.c  mtk_mt2701_hdmi_phy.c
mtk_cec.c  mtk_dpi.c         mtk_drm_ddp.h       mtk_drm_fb.c        mtk_drm_plane.h  mtk_hdmi_phy.c  mtk_mt8173_hdmi_phy.c
mtk_cec.h  mtk_dpi_regs.h    mtk_drm_ddp_comp.c  mtk_drm_fb.h        mtk_dsi.c        mtk_hdmi_phy.h
hacker@commands~an-epic-filesystem-quest:/opt/linux/linux-5.4/drivers/gpu/drm/mediatek$ cat EVIDENCE 
Great sleuthing!
The next clue is in: /usr/share/racket/pkgs/scribble-doc/scribblings/scribble

The next clue is **hidden** --- its filename starts with a '.' character. You'll need to look for it using special options to 'ls'.
hacker@commands~an-epic-filesystem-quest:/opt/linux/linux-5.4/drivers/gpu/drm/mediatek$ cd /usr/share/racket/pkgs/scribble-doc/scribblings/scribble/
hacker@commands~an-epic-filesystem-quest:/usr/share/racket/pkgs/scribble-doc/scribblings/scribble$ ls -a
.                   config.scrbl          demo-s2.scrbl          inbox.tex          manual.scrbl            sigplan.scrbl
..                  core.scrbl            demo.scrbl             info.rkt           plt.scrbl               srcdoc.scrbl
.REVELATION         decode.scrbl          doclang.scrbl          internals.scrbl    reader-internals.scrbl  struct-hierarchy.rkt
acmart.scrbl        demo-class.scrbl      docreader.scrbl        jfp.scrbl          reader.scrbl            struct.scrbl
base.scrbl          demo-m1.scrbl         eval.scrbl             layers.scrbl       renderer.scrbl          tag.scrbl
basic.scrbl         demo-m2.scrbl         examples.scrbl         lncs.scrbl         report.scrbl            text.scrbl
blueboxes.scrbl     demo-manual-m1.scrbl  generic.scrbl          lp-ex-doc.scrbl    running.scrbl           utils.rkt
bnf.scrbl           demo-manual-m2.scrbl  getting-started.scrbl  lp-ex.rkt          scheme.scrbl            xref.scrbl
book.scrbl          demo-manual-s1.scrbl  how-to-paper.scrbl     lp.css             scribble-pp.scrbl
class-diagrams.rkt  demo-manual-s2.scrbl  how-to.scrbl           lp.scrbl           scribble.scrbl
compat.scrbl        demo-manual.scrbl     html.scrbl             lp.tex             shaded.css
compiled            demo-s1.scrbl         inbox.css              manual-stub.scrbl  shaded.tex
hacker@commands~an-epic-filesystem-quest:/usr/share/racket/pkgs/scribble-doc/scribblings/scribble$ cat .REVELATION 
```
**Output:**
```bash
CONGRATULATIONS! Your perserverence has paid off, and you have found the flag!
It is: pwn.college{M9yAbCPc2C0RD5Mjjew9ok-fTUN.QX5IDO0wCM3UzNzEzW}
```
