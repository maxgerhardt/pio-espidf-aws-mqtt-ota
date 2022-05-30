set(COMPONENT_SRCS 
	"app_main.c"
	"ota_demo_core_mqtt.c"
	"mqtt_subscription_manager.c"
	)

set(COMPONENT_ADD_INCLUDEDIRS
	"."
	"${PROJECT_DIR}/components/common/logging/"
	)

idf_component_register(SRCS "${COMPONENT_SRCS}"
					   INCLUDE_DIRS ${COMPONENT_ADD_INCLUDEDIRS}
					  )

target_add_binary_data(${COMPONENT_TARGET} "certs/root_cert_auth.pem" TEXT)
target_add_binary_data(${COMPONENT_TARGET} "certs/client.crt" TEXT)
target_add_binary_data(${COMPONENT_TARGET} "certs/client.key" TEXT)
target_add_binary_data(${COMPONENT_TARGET} "certs/aws_codesign.crt" TEXT)
