## ----------------------------------------------------------- ##
## Don't touch the next line unless you know what you're doing.##
## ----------------------------------------------------------- ##

# Name of the module
LOCAL_NAME := cust_src/app/ftp

# List of submodules which contain code we need to include in the final lib
LOCAL_API_DEPENDS := \

LOCAL_ADD_INCLUDE := \
                    platform/std_inc \
                    platform/OpenAT_inc \
					api/include \
					cust_src/app/ftp/inc


# Set this to any non-null string to signal a module which 
# generates a binary (must contain a "main" entry point). 
# If left null, only a library will be generated.
IS_ENTRY_POINT := no

## ------------------------------------ ##
## 	Add your custom flags here          ##
## ------------------------------------ ##
MYCFLAGS += 

## ------------------------------------- ##
##	List all your sources here           ##
## ------------------------------------- ##
ifeq ($(strip $(IOT_SDK_USE_FTP)), TRUE)
C_SRC := ${notdir ${wildcard src/ftplib.c}}
else
C_SRC := ${notdir ${wildcard src/*.c}}
endif

## ------------------------------------- ##
##  Do Not touch below this line         ##
## ------------------------------------- ##
include ${SOFT_WORKDIR}/platform/compilation/cust_rules.mk