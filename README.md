# CMake Create Python Virtual Environment
CMake function to generate a python virtual environment


# Usage

	set(VENV_DIR "${CMAKE_BINARY_DIR}")
	set(VENV_NAME "venv")
	
	include(CreatePythonVenv)
	CreatePythonVenv(${VENV_DIR} ${VENV_NAME} VENV_PATH "${CMAKE_SOURCE_DIR}/requirements.txt")
	
	# Can now run python from within venv using VENV_PATH variable
	add_custom_command(TARGET COMMAND ${VENV_PATH} hello_world.py)
