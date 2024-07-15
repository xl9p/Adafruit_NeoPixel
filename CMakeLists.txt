cmake_minimum_required(VERSION 3.13)

if(ESP_PLATFORM)
  file(GLOB_RECURSE ADAFRUIT_NEOPIXEL
    "src/*.*"
  )

  idf_component_register(
    SRCS ${ADAFRUIT_NEOPIXEL} 
    INCLUDE_DIRS src 
    REQUIRES arduino
  )

  return()
endif()
