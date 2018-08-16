# Preparation
SourceCode/stacktrace/wireshake pcap file


# Recording
- wplus
	+ WSP hook
		- [#wplus.lrp](http://myd-vm16692.hpeswlab.net:8080/source/xref/LT-CORE-master/app/Protocols/CustomApi/static/dat/protocols/wplus.lrp)
		- [#wplusSetupWSPHooks](http://myd-vm16692.hpeswlab.net:8080/source/s?refs=wplusSetupWSPHooks&project=LT-CORE-master) fill function table 
		- take wplusWSPConnectAlternate callstack as a example 
- Inproc proxy
 	+ Non-SSL
		- [#initialize proxy](http://myd-vm16692.hpeswlab.net:8080/source/s?refs=wplus_initialize_proxy&project=LT-CORE-master)
		- [#register proxy](http://myd-vm16692.hpeswlab.net:8080/source/search?q=&defs=&refs=wplus_register_socket_proxy_wsp_connect&path=&hist=&type=&project=LT-CORE-master)
		- serverProxy/clientProxy 
		- [#process client to server](http://myd-vm16692.hpeswlab.net:8080/source/search?q=sph_process_client_to_server_data&project=LT-CORE-master)
		- [#process server to client](http://myd-vm16692.hpeswlab.net:8080/source/search?q=sph_process_client_to_server_data&project=LT-CORE-master)
		- [#protocol process client to server](http://myd-vm16692.hpeswlab.net:8080/source/search?q=&defs=protocol_process_client_to_server_data&refs=&path=&hist=&type=&project=LT-CORE-master)
		- [#protocol process server to client](http://myd-vm16692.hpeswlab.net:8080/source/s?defs=protocol_process_server_to_client_data&project=LT-CORE-master)
 	+ SSL
		- [#openssl proxy session thread](http://myd-vm16692.hpeswlab.net:8080/source/s?refs=openssl_setup_ssl2way_proxy_session_thread&project=LT-CORE-master)
		- serverProxy.ssl/clientProxy.ssl setting
		- Fake Certificate 

- Analyzer
 	+ ProtocolAnalyzer defined in lrp file
 	+ take CProtoHttpAnalyzer::ProcessClientToServerData as example
 	+ info of decompressed events file

