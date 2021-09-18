# select the 3D backend for sokol_gfx.h and sokol_app.h
add_definitions(-D${sokol_backend})

fips_ide_group(Samples)
fips_begin_app(app windowed)
    fips_vs_warning_level(3)
    fips_files(main.cc)
    fips_deps(sokol imgui)
    if (FIPS_IOS)
        fips_files(ios-info.plist)
    endif()
fips_end_app()

endif() # FIPS_UWP
