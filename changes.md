# ciot_c Release

### Changes

**Sparkplug B Protocol Integration**

* Added a new subdirectory `examples/sparkplugb` to the build system (`CMakelists.txt` and `common/Common.cmake`) and created its own CMake configuration for proper compilation and linking. [[1]](diffhunk://#diff-c34bbe988fbe83ad25dc3eb04cba40a8cc1d81f069b1773b76de741e5612cb70R13) [[2]](diffhunk://#diff-78b68c39a17a613575235e3e4c02fc418b4d1162bff76903516260f43e20828bR19) [[3]](diffhunk://#diff-33a86eb082877b72e29179975da4fa91223d7a430dc91e8c8ecf9ff0eb9a860fR1-R25)
* Added Sparkplug B protocol buffer options (`src/proto/sparkplug_b.options`) and ensured the Makefile generates nanopb source files for Sparkplug B messages, with dedicated targets for regeneration. [[1]](diffhunk://#diff-76ed074a9305c04054cdebb9e9aad2d818052b07091de1f20cad0bbac34ffb52R5-R17) [[2]](diffhunk://#diff-0b720f7da8f2f0f409a0d431f18303ed39f2a847e455727364edc9124e7e42e7R1-R58)
* Added the generated nanopb source file for Sparkplug B messages (`src/proto/sparkplug-b/proto/v1/sparkplug_b.pb.c`).

**Example Application: Sparkplug B Publisher**

* Implemented a new example application (`examples/sparkplugb/main.c`, `main.h`, and `ciot_custom_config.h`) that initializes CIoT interfaces, configures MQTT and NTP, and publishes Sparkplug B NBIRTH, DBIRTH, and DDATA messages to an MQTT broker. The example demonstrates serialization and publishing of Sparkplug B payloads. [[1]](diffhunk://#diff-c1fa74821c203c618ba8d4f360445fdde901e6b90c3cd57ed8e4395722f1c813R1-R239) [[2]](diffhunk://#diff-71963ef521523109206df77a375c64c91d527329aeec5ad0c29488c5e8140386R1-R63) [[3]](diffhunk://#diff-99776b59ae2656af945dc19c5a2617824f38759e1ec2442998b5d77b4caa44c9R1-R53)