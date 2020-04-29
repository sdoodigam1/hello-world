# maven-project

Simple Maven Project

# Environment Variables

| Name                        	| Description                                                                                                                                                                                                                                                	| Default Value 	| Notes                                                                                                                  	|
|-----------------------------	|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------	|---------------	|------------------------------------------------------------------------------------------------------------------------	|
| CAS_ENCRYPT_MONGO_KEY       	| CAS stores the MongoDB password on disk so this is a key that  encrypts a cipher of that password                                                                                                                                                          	|               	| Required, must be set or modified by user                                                                              	|
| MONGO_INITDB_ROOT_PASSWORD  	| MongoDB password, please change this before starting containers                                                                                                                                                                                            	|               	| Required, must be set or modified by user                                                                              	|
| VECTR_DATA_KEY              	| Encryption key for sensitive data stored in VECTR database  such as TAXII passwords                                                                                                                                                                        	|               	| Required, must be set or modified by user                                                                              	|
| COMPOSE_PROJECT_NAME        	| appended to the created docker containers                                                                                                                                                                                                                  	|               	| User-definable, may be modified by user but unnecessary to run application                                             	|
| VECTR_CONTAINER_LOG_LEVEL   	| Log level for container scripts (for now, this should probably apply log level changes across the board?)                                                                                                                                                  	|               	| User-definable, may be modified by user but unnecessary to run application                                             	|
| VECTR_HOSTNAME              	| Hostname to access the VECTR application                                                                                                                                                                                                                   	|               	| User-definable, may be modified by user but unnecessary to run application                                             	|
| VECTR_HTTP_HEADER_SERVER    	| Server name in HTTP headers                                                                                                                                                                                                                                	|               	| User-definable, may be modified by user but unnecessary to run application                                             	|
| VECTR_NETWORK_SUBNET        	| Subnet for VECTR docker container network                                                                                                                                                                                                                  	|               	| User-definable, may be modified by user but unnecessary to run application                                             	|
| CA_PASS                     	| Password for user-supplied CA certificates if they are present in user directory/volume and in use                                                                                                                                                         	|               	| May be modified by user under extreme configuration conditions or by development team - unlikely to be used by clients 	|
| CA_PEM_FILE                 	| CA PEM certificate filename                                                                                                                                                                                                                                	|               	| May be modified by user under extreme configuration conditions or by development team - unlikely to be used by clients 	|
| CA_KEY_FILE                 	| CA KEY filename                                                                                                                                                                                                                                            	|               	| May be modified by user under extreme configuration conditions or by development team - unlikely to be used by clients 	|
| CLASSPATH                   	| The Tomcat Java classpath                                                                                                                                                                                                                                  	|               	| May be modified by user under extreme configuration conditions or by development team - unlikely to be used by clients 	|
| DEFAULT_CERT_PATH           	| Certificates in use are deployed to this directory for  persistence                                                                                                                                                                                        	|               	| May be modified by user under extreme configuration conditions or by development team - unlikely to be used by clients 	|
| DEFAULT_CA_PATH             	| The internal path to CA certificate files                                                                                                                                                                                                                  	|               	| May be modified by user under extreme configuration conditions or by development team - unlikely to be used by clients 	|
| MONGO_INITDB_ROOT_USERNAME  	| MongoDB default username, don’t change this - it’s not really configurable                                                                                                                                                                                 	|               	| May be modified by user under extreme configuration conditions or by development team - unlikely to be used by clients 	|
| TOMCAT_CONF_DIR             	| Path to internal tomcat container configuration path for VECTR application                                                                                                                                                                                 	|               	| May be modified by user under extreme configuration conditions or by development team - unlikely to be used by clients 	|
| USER_CA_PATH                	| Path to user-specified CA file. (don’t change this without changing  code, it’s expected to be in a certain spot)                                                                                                                                          	|               	| May be modified by user under extreme configuration conditions or by development team - unlikely to be used by clients 	|
| USER_CERT_PATH              	| Path to user-specified application certificates (don’t change this without changing code, it’s expected to be in a certain spot)                                                                                                                           	|               	| May be modified by user under extreme configuration conditions or by development team - unlikely to be used by clients 	|
| VECTR_CERT_SSL_CRT          	| CTR application certificate filename                                                                                                                                                                                                                       	|               	| May be modified by user under extreme configuration conditions or by development team - unlikely to be used by clients 	|
| VECTR_CERT_SSL_KEY          	| VECTR application certificate key filename                                                                                                                                                                                                                 	|               	| May be modified by user under extreme configuration conditions or by development team - unlikely to be used by clients 	|
| VECTR_CONF                  	| Configuration directory for some miscellaneous VECTR config files                                                                                                                                                                                          	|               	| May be modified by user under extreme configuration conditions or by development team - unlikely to be used by clients 	|
| VECTR_CONTAINER_DEPLOY      	| Internal Docker Tomcat container location where application  is deployed                                                                                                                                                                                   	|               	| May be modified by user under extreme configuration conditions or by development team - unlikely to be used by clients 	|
| VECTR_DATASETS_CTI_PATH     	| Path to MITRE CTI datasets path internal to container                                                                                                                                                                                                      	|               	| May be modified by user under extreme configuration conditions or by development team - unlikely to be used by clients 	|
| VECTR_DATASETS_CTI_FILENAME 	| MITRE Enterprise ATT&CK json internal filename - mitre-cti.json                                                                                                                                                                                            	|               	| May be modified by user under extreme configuration conditions or by development team - unlikely to be used by clients 	|
| VECTR_DATASETS_CTI_FULLPATH 	| Full path to Enterprise ATT&CK json file                                                                                                                                                                                                                   	|               	| May be modified by user under extreme configuration conditions or by development team - unlikely to be used by clients 	|
| VECTR_DEFAULT_INTERNAL_PORT 	| Internal container port for VECTR application                                                                                                                                                                                                              	|               	| May be modified by user under extreme configuration conditions or by development team - unlikely to be used by clients 	|
| VECTR_EXTERNAL_HOSTNAME     	| This is the FQDN of the VECTR service URL specified in the  CAS service registration configuration. Only set this if you are running VECTR and CAS behind a load balancer or proxy and VECTR's external facing hostname is not the same as VECTR_HOSTNAME. 	|               	| May be modified by user under extreme configuration conditions or by development team - unlikely to be used by clients 	|
| VECTR_HOME                  	| Home folder for VECTR internal docker tomcat container user (application  doesn’t run as this user yet)                                                                                                                                                    	|               	| May be modified by user under extreme configuration conditions or by development team - unlikely to be used by clients 	|
| VECTR_MONGO_PORT            	| Internal docker network port for MongoDB instance                                                                                                                                                                                                          	|               	| May be modified by user under extreme configuration conditions or by development team - unlikely to be used by clients 	|
| VECTR_TAXII_CERTS_CA_PATH   	| Path to certificate for TAXII server (only for development)                                                                                                                                                                                                	|               	| May be modified by user under extreme configuration conditions or by development team - unlikely to be used by clients 	|
| VECTR_USER_DIR              	| The VECTR user directory internal to the container                                                                                                                                                                                                         	|               	| May be modified by user under extreme configuration conditions or by development team - unlikely to be used by clients 	|
| VECTR_VERSION               	| Set at build-time with embedded VECTR version.                                                                                                                                                                                                             	|               	| Set by application or build process, should not be modified by users                                                   	|
| VECTR_BUILD_DATE            	| Set at build-time with build date.                                                                                                                                                                                                                         	|               	| Set by application or build process, should not be modified by users                                                   	|
|                             	|                                                                                                                                                                                                                                                            	|               	|                                                                                                                        	|
