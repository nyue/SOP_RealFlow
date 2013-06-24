CMAKE_MINIMUM_REQUIRED(VERSION 2.8)

PROJECT ( Houdini_RealFlow )

FIND_PACKAGE ( HDK )
INCLUDE_DIRECTORIES ( ${HDK_INCLUDE_DIR} )

# LINKER FLAGS -undefined dynamic_lookup
ADD_EXECUTABLE ( dump_rf_part
  dump_rf_part.C
  )

ADD_EXECUTABLE ( dump_rf_mesh
  dump_rf_mesh.C
  )

ADD_EXECUTABLE ( dump_rf_sd
  dump_rf_sd.C
  )

ADD_EXECUTABLE ( dump_rf_rwc
  dump_rf_rwc.C
  )

HDK_ADD_LIBRARY ( SOP_RF_Import 
  SOP_RF_Import.C
)

HDK_ADD_LIBRARY ( SOP_RF_Export 
  SOP_RF_Export.C
)

