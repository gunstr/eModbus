list(APPEND EMODBUS_PRIV_REQUIRES
    AsyncTCP
)

list(APPEND EMODBUS_PRIV_REQUIRES
        espressif__arduino-esp32
    )

# List all the source files
set(SRCS
    src/CoilData.cpp
    src/Logging.cpp
    src/ModbusClient.cpp
    src/ModbusClientRTU.cpp
    src/ModbusClientTCPasync.cpp
    src/ModbusClientTCP.cpp
    src/ModbusMessage.cpp
    src/ModbusServer.cpp
    src/ModbusServerRTU.cpp
    src/ModbusServerTCPasync.cpp
    src/ModbusTypeDefs.cpp
    src/RTUutils.cpp
)

# List all the include directories
set(INCLUDE_DIRS
    "src"
)

# Register the component
idf_component_register(
    SRCS ${SRCS}
    INCLUDE_DIRS ${INCLUDE_DIRS}
    PRIV_REQUIRES ${EMODBUS_PRIV_REQUIRES}
)