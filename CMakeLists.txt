project(rememberthemilk-simple)

find_package(KDE4 REQUIRED)
include(KDE4Defaults)

add_definitions(${QT_DEFINITIONS} ${KDE4_DEFINITIONS})
include_directories(${CMAKE_SOURCE_DIR} ${CMAKE_BINARY_DIR} ${KDE4_INCLUDES})

set(rememberthemilk-simple_SRCS 
      rememberthemilk-simple.cpp
      taskitem.cpp
      taskitemdelegate.cpp
      taskeditor.cpp
      taskmodel.cpp
      tasksortfilter.cpp)
      
kde4_add_ui_files(rememberthemilk-simple_SRCS authenticate.ui general.ui)

kde4_add_plugin(plasma_applet_rememberthemilk-simple ${rememberthemilk-simple_SRCS})
target_link_libraries(plasma_applet_rememberthemilk-simple 
                      ${KDE4_PLASMA_LIBS}
                      ${KDE4_SOLID_LIBS}
                      ${KDE4_KDEUI_LIBS}
                     )
 
install(TARGETS plasma_applet_rememberthemilk-simple
        DESTINATION ${PLUGIN_INSTALL_DIR})
 
install(FILES plasma-applet-rememberthemilk-simple.desktop
        DESTINATION ${SERVICES_INSTALL_DIR})
