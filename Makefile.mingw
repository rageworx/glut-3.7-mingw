################################################################################
# Makefile for libglut32 version 3.7 of MinGW-W64
# -----------------------------------------------------------------------------
# Written by Raphael Kim ( rageworx@gmail.com, rage.kim@gmail.com )
################################################################################

PREFIX=
GCC=$(PREFIX)gcc
GPP=$(PREFIX)g++

CFLAGS =-mthreads -O3 
CFLAGS+=-Iinclude 
CFLAGS+=-DWIN32 -D_WIN32 -DNDEBUG -D_WINDOWS -D_MBCS -D_USRDLL -DGLUT32_EXPORTS 
CFLAGS+=-UGLUT_USE_SGI_OPENGL

OBJS =lib/glut/glut_8x13.o 
OBJS+=lib/glut/glut_9x15.o 
OBJS+=lib/glut/glut_bitmap.o 
OBJS+=lib/glut/glut_bwidth.o 
OBJS+=lib/glut/glut_cindex.o 
OBJS+=lib/glut/glut_cmap.o 
OBJS+=lib/glut/glut_cursor.o 
OBJS+=lib/glut/glut_dials.o 
OBJS+=lib/glut/glut_dstr.o 
OBJS+=lib/glut/glut_event.o 
OBJS+=lib/glut/glut_ext.o 
OBJS+=lib/glut/glut_fullscrn.o 
OBJS+=lib/glut/glut_gamemode.o 
OBJS+=lib/glut/glut_get.o 
OBJS+=lib/glut/glut_glxext.o 
OBJS+=lib/glut/glut_hel10.o 
OBJS+=lib/glut/glut_hel12.o 
OBJS+=lib/glut/glut_hel18.o 
OBJS+=lib/glut/glut_init.o 
OBJS+=lib/glut/glut_input.o 
OBJS+=lib/glut/glut_joy.o 
OBJS+=lib/glut/glut_key.o 
OBJS+=lib/glut/glut_keyctrl.o 
OBJS+=lib/glut/glut_keyup.o 
OBJS+=lib/glut/glut_mesa.o 
OBJS+=lib/glut/glut_modifier.o 
OBJS+=lib/glut/glut_mroman.o 
OBJS+=lib/glut/glut_overlay.o 
OBJS+=lib/glut/glut_roman.o 
OBJS+=lib/glut/glut_shapes.o 
OBJS+=lib/glut/glut_space.o 
OBJS+=lib/glut/glut_stroke.o 
OBJS+=lib/glut/glut_swap.o 
OBJS+=lib/glut/glut_swidth.o 
OBJS+=lib/glut/glut_tablet.o 
OBJS+=lib/glut/glut_teapot.o 
OBJS+=lib/glut/glut_tr10.o 
OBJS+=lib/glut/glut_tr24.o 
OBJS+=lib/glut/glut_util.o 
OBJS+=lib/glut/glut_vidresize.o 
OBJS+=lib/glut/glut_warp.o 
OBJS+=lib/glut/glut_win.o 
OBJS+=lib/glut/glut_winmisc.o 
OBJS+=lib/glut/win32_glx.o 
OBJS+=lib/glut/win32_menu.o 
OBJS+=lib/glut/win32_util.o 
OBJS+=lib/glut/win32_winproc.o 
OBJS+=lib/glut/win32_x11.o

TARGET_N=glut32
TARGET_A=lib/glut/lib$(TARGET_N).a
TARGET_D=lib/glut/$(TARGET_N).dll
TARGET_SA=lib/glut/lib$(TARGET_N)static.a

# it must be running on MSYS, or MSYS2.
INSTALL_B=/usr/local/bin
INSTALL_I=/usr/local/include
INSTALL_L=/usr/local/lib

LFLAGS =-mthreads -O3 
LFLAGS+=-lkernel32 -luser32 -lgdi32 -lwinspool -lcomdlg32 -ladvapi32 -lshell32 -lole32 -loleaut32 
LFLAGS+=-luuid -lodbc32 -lodbccp32 -lwinmm -lglu32 -lopengl32 
#LFLAGS+=-enable-auto-import -Wl,--out-implib,$(TARGET_A)
LFLAGS+= -Wl,--out-implib,$(TARGET_A)

all: $(TARGET_D) $(TARGET_A)

static: $(TARGET_SA)

$(TARGET_SA): $(OBJS)
	@echo "Generating $@ ..."
	@$(AR) -q $@ $(OBJS)
	
$(TARGET_D) $(TARGET_A): $(OBJS)
	@echo "Generating $@ ..."
	@$(GCC) -shared -o $(TARGET_D) $(OBJS) $(LFLAGS)

lib/glut/glut_8x13.o: lib/glut/glut_8x13.c lib/glut/glutbitmap.h
	@echo "Compiling $< ..."
	@$(GCC) -c -o $@ $< $(CFLAGS)

lib/glut/glut_9x15.o: lib/glut/glut_9x15.c lib/glut/glutbitmap.h
	@echo "Compiling $< ..."
	@$(GCC) -c -o $@ $< $(CFLAGS)

lib/glut/glut_bitmap.o: lib/glut/glut_bitmap.c lib/glut/glutint.h lib/glut/glutbitmap.h
	@echo "Compiling $< ..."
	@$(GCC) -c -o $@ $< $(CFLAGS)

lib/glut/glut_bwidth.o: lib/glut/glut_bwidth.c lib/glut/glutint.h lib/glut/glutbitmap.h
	@echo "Compiling $< ..."
	@$(GCC) -c -o $@ $< $(CFLAGS)

lib/glut/glut_cindex.o: lib/glut/glut_cindex.c lib/glut/glutint.h
	@echo "Compiling $< ..."
	@$(GCC) -c -o $@ $< $(CFLAGS)

lib/glut/glut_cmap.o: lib/glut/glut_cmap.c lib/glut/glutint.h lib/glut/layerutil.h
	@echo "Compiling $< ..."
	@$(GCC) -c -o $@ $< $(CFLAGS)

lib/glut/glut_cursor.o: lib/glut/glut_cursor.c lib/glut/glutint.h
	@echo "Compiling $< ..."
	@$(GCC) -c -o $@ $< $(CFLAGS)

lib/glut/glut_dials.o: lib/glut/glut_dials.c lib/glut/glutint.h
	@echo "Compiling $< ..."
	@$(GCC) -c -o $@ $< $(CFLAGS)

lib/glut/glut_dstr.o: lib/glut/glut_dstr.c lib/glut/glutint.h
	@echo "Compiling $< ..."
	@$(GCC) -c -o $@ $< $(CFLAGS)

lib/glut/glut_event.o: lib/glut/glut_event.c lib/glut/glutint.h
	@echo "Compiling $< ..."
	@$(GCC) -c -o $@ $< $(CFLAGS)

lib/glut/glut_ext.o: lib/glut/glut_ext.c lib/glut/glutint.h
	@echo "Compiling $< ..."
	@$(GCC) -c -o $@ $< $(CFLAGS)

lib/glut/glut_fullscrn.o: lib/glut/glut_fullscrn.c lib/glut/glutint.h
	@echo "Compiling $< ..."
	@$(GCC) -c -o $@ $< $(CFLAGS)

lib/glut/glut_gamemode.o: lib/glut/glut_gamemode.c lib/glut/glutint.h
	@echo "Compiling $< ..."
	@$(GCC) -c -o $@ $< $(CFLAGS)

lib/glut/glut_get.o: lib/glut/glut_get.c lib/glut/glutint.h
	@echo "Compiling $< ..."
	@$(GCC) -c -o $@ $< $(CFLAGS)

lib/glut/glut_glxext.o: lib/glut/glut_glxext.c lib/glut/glutint.h
	@echo "Compiling $< ..."
	@$(GCC) -c -o $@ $< $(CFLAGS)

lib/glut/glut_hel10.o: lib/glut/glut_hel10.c lib/glut/glutbitmap.h
	@echo "Compiling $< ..."
	@$(GCC) -c -o $@ $< $(CFLAGS)

lib/glut/glut_hel12.o: lib/glut/glut_hel12.c lib/glut/glutbitmap.h
	@echo "Compiling $< ..."
	@$(GCC) -c -o $@ $< $(CFLAGS)

lib/glut/glut_hel18.o: lib/glut/glut_hel18.c lib/glut/glutbitmap.h
	@echo "Compiling $< ..."
	@$(GCC) -c -o $@ $< $(CFLAGS)

lib/glut/glut_init.o: lib/glut/glut_init.c lib/glut/glutint.h
	@echo "Compiling $< ..."
	@$(GCC) -c -o $@ $< $(CFLAGS)

lib/glut/glut_input.o: lib/glut/glut_input.c lib/glut/glutint.h
	@echo "Compiling $< ..."
	@$(GCC) -c -o $@ $< $(CFLAGS)

lib/glut/glut_joy.o: lib/glut/glut_joy.c lib/glut/glutint.h
	@echo "Compiling $< ..."
	@$(GCC) -c -o $@ $< $(CFLAGS)

lib/glut/glut_key.o: lib/glut/glut_key.c lib/glut/glutint.h
	@echo "Compiling $< ..."
	@$(GCC) -c -o $@ $< $(CFLAGS)

lib/glut/glut_keyctrl.o: lib/glut/glut_keyctrl.c lib/glut/glutint.h
	@echo "Compiling $< ..."
	@$(GCC) -c -o $@ $< $(CFLAGS)

lib/glut/glut_keyup.o: lib/glut/glut_keyup.c lib/glut/glutint.h
	@echo "Compiling $< ..."
	@$(GCC) -c -o $@ $< $(CFLAGS)

lib/glut/glut_mesa.o: lib/glut/glut_mesa.c lib/glut/glutint.h
	@echo "Compiling $< ..."
	@$(GCC) -c -o $@ $< $(CFLAGS)

lib/glut/glut_modifier.o: lib/glut/glut_modifier.c lib/glut/glutint.h
	@echo "Compiling $< ..."
	@$(GCC) -c -o $@ $< $(CFLAGS)

lib/glut/glut_mroman.o: lib/glut/glut_mroman.c lib/glut/glutstroke.h
	@echo "Compiling $< ..."
	@$(GCC) -c -o $@ $< $(CFLAGS)

lib/glut/glut_overlay.o: lib/glut/glut_overlay.c lib/glut/glutint.h lib/glut/layerutil.h
	@echo "Compiling $< ..."
	@$(GCC) -c -o $@ $< $(CFLAGS)

lib/glut/glut_roman.o: lib/glut/glut_roman.c lib/glut/glutstroke.h
	@echo "Compiling $< ..."
	@$(GCC) -c -o $@ $< $(CFLAGS)

lib/glut/glut_shapes.o: lib/glut/glut_shapes.c lib/glut/glutint.h
	@echo "Compiling $< ..."
	@$(GCC) -c -o $@ $< $(CFLAGS)

lib/glut/glut_space.o: lib/glut/glut_space.c lib/glut/glutint.h
	@echo "Compiling $< ..."
	@$(GCC) -c -o $@ $< $(CFLAGS)

lib/glut/glut_stroke.o: lib/glut/glut_stroke.c lib/glut/glutint.h lib/glut/glutstroke.h
	@echo "Compiling $< ..."
	@$(GCC) -c -o $@ $< $(CFLAGS)

lib/glut/glut_swap.o: lib/glut/glut_swap.c lib/glut/glutint.h
	@echo "Compiling $< ..."
	@$(GCC) -c -o $@ $< $(CFLAGS)

lib/glut/glut_swidth.o: lib/glut/glut_swidth.c lib/glut/glutint.h lib/glut/glutstroke.h
	@echo "Compiling $< ..."
	@$(GCC) -c -o $@ $< $(CFLAGS)

lib/glut/glut_tablet.o: lib/glut/glut_tablet.c lib/glut/glutint.h
	@echo "Compiling $< ..."
	@$(GCC) -c -o $@ $< $(CFLAGS)

lib/glut/glut_teapot.o: lib/glut/glut_teapot.c lib/glut/glutint.h
	@echo "Compiling $< ..."
	@$(GCC) -c -o $@ $< $(CFLAGS)

lib/glut/glut_tr10.o: lib/glut/glut_tr10.c lib/glut/glutbitmap.h
	@echo "Compiling $< ..."
	@$(GCC) -c -o $@ $< $(CFLAGS)

lib/glut/glut_tr24.o: lib/glut/glut_tr24.c lib/glut/glutbitmap.h
	@echo "Compiling $< ..."
	@$(GCC) -c -o $@ $< $(CFLAGS)

lib/glut/glut_util.o: lib/glut/glut_util.c lib/glut/glutint.h
	@echo "Compiling $< ..."
	@$(GCC) -c -o $@ $< $(CFLAGS)

lib/glut/glut_vidresize.o: lib/glut/glut_vidresize.c lib/glut/glutint.h
	@echo "Compiling $< ..."
	@$(GCC) -c -o $@ $< $(CFLAGS)

lib/glut/glut_warp.o: lib/glut/glut_warp.c lib/glut/glutint.h
	@echo "Compiling $< ..."
	@$(GCC) -c -o $@ $< $(CFLAGS)

lib/glut/glut_win.o: lib/glut/glut_win.c lib/glut/glutint.h
	@echo "Compiling $< ..."
	@$(GCC) -c -o $@ $< $(CFLAGS)

lib/glut/glut_winmisc.o: lib/glut/glut_winmisc.c lib/glut/glutint.h
	@echo "Compiling $< ..."
	@$(GCC) -c -o $@ $< $(CFLAGS)
	
lib/glut/win32_glx.o: lib/glut/win32_glx.c lib/glut/glutint.h
	@echo "Compiling $< ..."
	@$(GCC) -c -o $@ $< $(CFLAGS)

lib/glut/win32_menu.o: lib/glut/win32_menu.c lib/glut/glutint.h
	@echo "Compiling $< ..."
	@$(GCC) -c -o $@ $< $(CFLAGS)

lib/glut/win32_util.o: lib/glut/win32_util.c lib/glut/glutint.h lib/glut/glutstroke.h lib/glut/glutbitmap.h
	@echo "Compiling $< ..."
	@$(GCC) -c -o $@ $< $(CFLAGS)

lib/glut/win32_winproc.o: lib/glut/win32_winproc.c lib/glut/glutint.h
	@echo "Compiling $< ..."
	@$(GCC) -c -o $@ $< $(CFLAGS)

lib/glut/win32_x11.o: lib/glut/win32_x11.c lib/glut/glutint.h
	@echo "Compiling $< ..."
	@$(GCC) -c -o $@ $< $(CFLAGS)

# GLUT 3.7 not contains windows Resource.
#lib/glut/resources.o: lib/glut/glut.rc lib/glut/glut.ico
#	windres lib/glut/glut.rc lib/glut/resources.o

lib/glut/glutbitmap.h: include/GL/glut.h

lib/glut/glutint.h: lib/glut/glutwin32.h include/GL/glut.h include/GL/glutf90.h

lib/glut/glutstroke.h: 

lib/glut/glutwin32.h: lib/glut/win32_x11.h lib/glut/win32_glx.h

lib/glut/layerutil.h: 

lib/glut/stroke.h: 

lib/glut/win32_glx.h: lib/glut/win32_x11.h

lib/glut/win32_x11.h: 

include/GL/glutf90.h: include/GL/glut.h

include/GL/glut.h:

install: $(TARGET_D) $(TARGET_A)
	@echo "Installing ..."
	@mkdir -p $(INSTALL_I)/GL
	@echo $(INSTALL_B)/$(TARGET_N).dll
	@cp -f $(TARGET_D) $(INSTALL_B)/$(TARGET_N).dll
	@cp -f include/GL/glut.h $(INSTALL_I)/GL/glut.h
	@cp -f lib/glut/lib$(TARGET_N).a $(INSTALL_L)/lib$(TARGET_N).a

test: install
	@echo "TEST"
	@$(GPP) -o progs/mesademos/gears.exe progs/mesademos/gears.c -I$(INSTALL_I) -L$(INSTALL_L) -mthreads -std=c++0x -O3 -lglut32 -lopengl32 -lglu32 -mwindows
	@progs/mesademos/gears.exe
	@echo "Done."

uninstall:
	@echo "Uninstalling ..."
	@rm --force --verbose $(INSTALL_B)/$(TARGET_N).dll
	@rm --force --verbose $(INSTALL_I)/GL/glut.h
	@rm --force --verbose $(INSTALL_L)/lib$(TARGET_N).a
	@echo "Done."

clean:
	@echo "Cleaning ..."
	@rm --force --verbose lib/glut/*.dll lib/glut/*.a lib/glut/*.o 
	@rm --force --verbose progs/mesademos/*.exe
	@echo "Done."
