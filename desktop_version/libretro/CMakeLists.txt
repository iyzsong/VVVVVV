# configure SDL2 for libretro
file(COPY SDL_config.h DESTINATION ${CMAKE_SOURCE_DIR}/../third_party/SDL/include)
file(COPY SDL_dynapi.h DESTINATION ${CMAKE_SOURCE_DIR}/../third_party/SDL/src/dynapi)

add_library(sdl2 STATIC
  ../../third_party/SDL/src/SDL.c
  ../../third_party/SDL/src/SDL_assert.c
  ../../third_party/SDL/src/SDL_dataqueue.c
  ../../third_party/SDL/src/SDL_error.c
  ../../third_party/SDL/src/SDL_guid.c
  ../../third_party/SDL/src/SDL_hints.c
  ../../third_party/SDL/src/SDL_list.c
  ../../third_party/SDL/src/SDL_log.c
  ../../third_party/SDL/src/SDL_utils.c
  ../../third_party/SDL/src/atomic/SDL_atomic.c
  ../../third_party/SDL/src/atomic/SDL_spinlock.c
  ../../third_party/SDL/src/audio/SDL_audio.c
  ../../third_party/SDL/src/audio/SDL_audiocvt.c
  ../../third_party/SDL/src/audio/SDL_audiodev.c
  ../../third_party/SDL/src/audio/SDL_audiotypecvt.c
  ../../third_party/SDL/src/audio/SDL_mixer.c
  ../../third_party/SDL/src/audio/SDL_wave.c
  ../../third_party/SDL/src/loadso/dlopen/SDL_sysloadso.c
  ../../third_party/SDL/src/core/linux/SDL_threadprio.c
  ../../third_party/SDL/src/filesystem/unix/SDL_sysfilesystem.c
  ../../third_party/SDL/src/cpuinfo/SDL_cpuinfo.c
  ../../third_party/SDL/src/dynapi/SDL_dynapi.c
  ../../third_party/SDL/src/events/SDL_clipboardevents.c
  ../../third_party/SDL/src/events/SDL_displayevents.c
  ../../third_party/SDL/src/events/SDL_dropevents.c
  ../../third_party/SDL/src/events/SDL_events.c
  ../../third_party/SDL/src/events/SDL_gesture.c
  ../../third_party/SDL/src/events/SDL_keyboard.c
  ../../third_party/SDL/src/events/SDL_keysym_to_scancode.c
  ../../third_party/SDL/src/events/SDL_mouse.c
  ../../third_party/SDL/src/events/SDL_quit.c
  ../../third_party/SDL/src/events/SDL_scancode_tables.c
  ../../third_party/SDL/src/events/SDL_touch.c
  ../../third_party/SDL/src/events/SDL_windowevents.c
  ../../third_party/SDL/src/events/imKStoUCS.c
  ../../third_party/SDL/src/file/SDL_rwops.c
  ../../third_party/SDL/src/joystick/SDL_gamecontroller.c
  ../../third_party/SDL/src/joystick/SDL_joystick.c
  ../../third_party/SDL/src/joystick/SDL_steam_virtual_gamepad.c
  ../../third_party/SDL/src/joystick/controller_type.c
  ../../third_party/SDL/src/joystick/dummy/SDL_sysjoystick.c
  ../../third_party/SDL/src/haptic/SDL_haptic.c
  ../../third_party/SDL/src/haptic/dummy/SDL_syshaptic.c
  ../../third_party/SDL/src/render/SDL_d3dmath.c
  ../../third_party/SDL/src/render/SDL_render.c
  ../../third_party/SDL/src/render/SDL_yuv_sw.c
  ../../third_party/SDL/src/render/opengl/SDL_render_gl.c
  ../../third_party/SDL/src/render/opengl/SDL_shaders_gl.c
  ../../third_party/SDL/src/render/opengles/SDL_render_gles.c
  ../../third_party/SDL/src/render/opengles2/SDL_render_gles2.c
  ../../third_party/SDL/src/render/opengles2/SDL_shaders_gles2.c
  ../../third_party/SDL/src/render/software/SDL_blendfillrect.c
  ../../third_party/SDL/src/render/software/SDL_blendline.c
  ../../third_party/SDL/src/render/software/SDL_blendpoint.c
  ../../third_party/SDL/src/render/software/SDL_drawline.c
  ../../third_party/SDL/src/render/software/SDL_drawpoint.c
  ../../third_party/SDL/src/render/software/SDL_render_sw.c
  ../../third_party/SDL/src/render/software/SDL_rotate.c
  ../../third_party/SDL/src/render/software/SDL_triangle.c
  ../../third_party/SDL/src/stdlib/SDL_crc16.c
  ../../third_party/SDL/src/stdlib/SDL_crc32.c
  ../../third_party/SDL/src/stdlib/SDL_getenv.c
  ../../third_party/SDL/src/stdlib/SDL_iconv.c
  ../../third_party/SDL/src/stdlib/SDL_malloc.c
  ../../third_party/SDL/src/stdlib/SDL_mslibc.c
  ../../third_party/SDL/src/stdlib/SDL_qsort.c
  ../../third_party/SDL/src/stdlib/SDL_stdlib.c
  ../../third_party/SDL/src/stdlib/SDL_string.c
  ../../third_party/SDL/src/stdlib/SDL_strtokr.c
  ../../third_party/SDL/src/thread/SDL_thread.c
  ../../third_party/SDL/src/thread/pthread/SDL_syscond.c
  ../../third_party/SDL/src/thread/pthread/SDL_sysmutex.c
  ../../third_party/SDL/src/thread/pthread/SDL_syssem.c
  ../../third_party/SDL/src/thread/pthread/SDL_systhread.c
  ../../third_party/SDL/src/thread/pthread/SDL_systls.c
  ../../third_party/SDL/src/timer/SDL_timer.c
  ../../third_party/SDL/src/timer/unix/SDL_systimer.c
  ../../third_party/SDL/src/video/SDL_RLEaccel.c
  ../../third_party/SDL/src/video/SDL_blit.c
  ../../third_party/SDL/src/video/SDL_blit_0.c
  ../../third_party/SDL/src/video/SDL_blit_1.c
  ../../third_party/SDL/src/video/SDL_blit_A.c
  ../../third_party/SDL/src/video/SDL_blit_N.c
  ../../third_party/SDL/src/video/SDL_blit_auto.c
  ../../third_party/SDL/src/video/SDL_blit_copy.c
  ../../third_party/SDL/src/video/SDL_blit_slow.c
  ../../third_party/SDL/src/video/SDL_bmp.c
  ../../third_party/SDL/src/video/SDL_clipboard.c
  ../../third_party/SDL/src/video/SDL_egl.c
  ../../third_party/SDL/src/video/SDL_fillrect.c
  ../../third_party/SDL/src/video/SDL_pixels.c
  ../../third_party/SDL/src/video/SDL_rect.c
  ../../third_party/SDL/src/video/SDL_shape.c
  ../../third_party/SDL/src/video/SDL_stretch.c
  ../../third_party/SDL/src/video/SDL_surface.c
  ../../third_party/SDL/src/video/SDL_video.c
  ../../third_party/SDL/src/video/SDL_vulkan_utils.c
  ../../third_party/SDL/src/video/SDL_yuv.c
  ../../third_party/SDL/src/video/yuv2rgb/yuv_rgb_lsx.c
  ../../third_party/SDL/src/video/yuv2rgb/yuv_rgb_sse.c
  ../../third_party/SDL/src/video/yuv2rgb/yuv_rgb_std.c
  ../../third_party/SDL/src/misc/SDL_url.c
  ../../third_party/SDL/src/misc/unix/SDL_sysurl.c
)
target_include_directories(sdl2 PUBLIC
  ../../third_party/SDL/include
)
