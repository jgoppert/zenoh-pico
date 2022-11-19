if(CONFIG_ZENOHPICO)

zephyr_library()

zephyr_library_compile_definitions(ZENOH_ZEPHYR)

zephyr_library_include_directories(
	../include
	../../../../zephyr/include/zephyr
	)

file(GLOB SOURCES "../src/*.c"
	"../src/api/*.c"
	"../src/net/*.c"
	"../src/collections/*.c"
	"../src/link/*.c"
	"../src/link/config/*.c"
	"../src/link/unicast/*.c"
	"../src/link/multicast/*.c"
	"../src/protocol/*.c"
	"../src/protocol/keyexpr/*.c"
	#"../src/session/*.c"
	"../src/system/*.c"
	#"../src/system/unix/*.c"
	"../src/transport/*.c"
	"../src/transport/common/*.c"
	"../src/transport/unicast/*.c"
	"../src/transport/unicast/link/*.c"
	"../src/transport/unicast/link/task/*.c"
	"../src/transport/multicast/*.c"
	"../src/transport/multicast/link/*.c"
	"../src/transport/multicast/link/task/*.c"
	"../src/utils/*.c"
)

zephyr_library_sources(${SOURCES})

endif()
