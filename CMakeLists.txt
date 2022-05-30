# The following five lines of boilerplate have to be in your project's
# CMakeLists in this exact order for cmake to work correctly
cmake_minimum_required(VERSION 3.16.0)

set(EXTRA_COMPONENT_DIRS $ENV{IDF_PATH}/examples/common_components/protocol_examples_common
						 "${CMAKE_CURRENT_LIST_DIR}/components/ota-for-aws-iot-embedded-sdk"
						 "${CMAKE_CURRENT_LIST_DIR}/components/coreMQTT"
						 "${CMAKE_CURRENT_LIST_DIR}/components/corePKCS11"
						 "${CMAKE_CURRENT_LIST_DIR}/components/backoffAlgorithm"
						 "${CMAKE_CURRENT_LIST_DIR}/components/common/posix_compat"
   )

include($ENV{IDF_PATH}/tools/cmake/project.cmake)
project(espidf-blink)
