
CC =	cl
CFLAGS =  -O2  -W4  -nologo -MT -Zi -DFD_SETSIZE=1024 -DNO_SYS_TYPES_H
CPP =	
LINK =	$(CC)


ALL_INCS = -I src/core \
	-I src/event \
	-I src/event/modules \
	-I src/os/win32 \
	-I objs/lib/pcre-8.40 \
	-I objs/lib/openssl/openssl/include \
	-I objs/lib/zlib \
	-I objs \
	-I src/http \
	-I src/http/modules


CORE_DEPS = src/core/nginx.h \
	src/core/ngx_config.h \
	src/core/ngx_core.h \
	src/core/ngx_log.h \
	src/core/ngx_palloc.h \
	src/core/ngx_array.h \
	src/core/ngx_list.h \
	src/core/ngx_hash.h \
	src/core/ngx_buf.h \
	src/core/ngx_queue.h \
	src/core/ngx_string.h \
	src/core/ngx_parse.h \
	src/core/ngx_parse_time.h \
	src/core/ngx_inet.h \
	src/core/ngx_file.h \
	src/core/ngx_crc.h \
	src/core/ngx_crc32.h \
	src/core/ngx_murmurhash.h \
	src/core/ngx_md5.h \
	src/core/ngx_sha1.h \
	src/core/ngx_rbtree.h \
	src/core/ngx_radix_tree.h \
	src/core/ngx_rwlock.h \
	src/core/ngx_slab.h \
	src/core/ngx_times.h \
	src/core/ngx_shmtx.h \
	src/core/ngx_connection.h \
	src/core/ngx_cycle.h \
	src/core/ngx_conf_file.h \
	src/core/ngx_module.h \
	src/core/ngx_resolver.h \
	src/core/ngx_open_file_cache.h \
	src/core/ngx_crypt.h \
	src/core/ngx_proxy_protocol.h \
	src/core/ngx_syslog.h \
	src/event/ngx_event.h \
	src/event/ngx_event_timer.h \
	src/event/ngx_event_posted.h \
	src/event/ngx_event_connect.h \
	src/event/ngx_event_pipe.h \
	src/os/win32/ngx_win32_config.h \
	src/os/win32/ngx_time.h \
	src/os/win32/ngx_errno.h \
	src/os/win32/ngx_alloc.h \
	src/os/win32/ngx_files.h \
	src/os/win32/ngx_shmem.h \
	src/os/win32/ngx_process.h \
	src/os/win32/ngx_atomic.h \
	src/os/win32/ngx_thread.h \
	src/os/win32/ngx_socket.h \
	src/os/win32/ngx_os.h \
	src/os/win32/ngx_user.h \
	src/os/win32/ngx_dlopen.h \
	src/os/win32/ngx_process_cycle.h \
	src/event/ngx_event_openssl.h \
	src/core/ngx_regex.h \
	objs/lib/pcre-8.40/pcre.h \
	objs/lib/openssl/openssl/include/openssl/ssl.h \
	objs/ngx_auto_config.h \
	objs/ngx_config.pch


CORE_INCS = -I src/core \
	-I src/event \
	-I src/event/modules \
	-I src/os/win32 \
	-I objs/lib/pcre-8.40 \
	-I objs/lib/openssl/openssl/include \
	-I objs/lib/zlib \
	-I objs


HTTP_DEPS = src/http/ngx_http.h \
	src/http/ngx_http_request.h \
	src/http/ngx_http_config.h \
	src/http/ngx_http_core_module.h \
	src/http/ngx_http_cache.h \
	src/http/ngx_http_variables.h \
	src/http/ngx_http_script.h \
	src/http/ngx_http_upstream.h \
	src/http/ngx_http_upstream_round_robin.h \
	src/http/modules/ngx_http_ssi_filter_module.h \
	src/http/modules/ngx_http_ssl_module.h


HTTP_INCS = -I src/http \
	-I src/http/modules


ADDON_DEPS = $(CORE_DEPS)                                             objs/lib/nginx-vod-module/vod/dash/edash_packager.h                objs/lib/nginx-vod-module/vod/hls/aes_cbc_encrypt.h                objs/lib/nginx-vod-module/vod/hls/eac3_encrypt_filter.h            objs/lib/nginx-vod-module/vod/hls/frame_encrypt_filter.h           objs/lib/nginx-vod-module/vod/hls/sample_aes_avc_filter.h          objs/lib/nginx-vod-module/vod/mp4/mp4_aes_ctr.h                    objs/lib/nginx-vod-module/vod/mp4/mp4_cbcs_encrypt.h               objs/lib/nginx-vod-module/vod/mp4/mp4_cenc_decrypt.h               objs/lib/nginx-vod-module/vod/mp4/mp4_cenc_encrypt.h               objs/lib/nginx-vod-module/vod/mp4/mp4_cenc_passthrough.h           objs/lib/nginx-vod-module/vod/mss/mss_playready.h                                                                       objs/lib/nginx-vod-module/ngx_async_open_file_cache.h                    objs/lib/nginx-vod-module/ngx_buffer_cache.h                             objs/lib/nginx-vod-module/ngx_buffer_cache_internal.h                    objs/lib/nginx-vod-module/ngx_child_http_request.h                       objs/lib/nginx-vod-module/ngx_file_reader.h                              objs/lib/nginx-vod-module/ngx_http_vod_conf.h                            objs/lib/nginx-vod-module/ngx_http_vod_dash.h                            objs/lib/nginx-vod-module/ngx_http_vod_dash_commands.h                   objs/lib/nginx-vod-module/ngx_http_vod_dash_conf.h                       objs/lib/nginx-vod-module/ngx_http_vod_hds.h                             objs/lib/nginx-vod-module/ngx_http_vod_hds_commands.h                    objs/lib/nginx-vod-module/ngx_http_vod_hds_conf.h                        objs/lib/nginx-vod-module/ngx_http_vod_hls.h                             objs/lib/nginx-vod-module/ngx_http_vod_hls_commands.h                    objs/lib/nginx-vod-module/ngx_http_vod_hls_conf.h                        objs/lib/nginx-vod-module/ngx_http_vod_module.h                          objs/lib/nginx-vod-module/ngx_http_vod_mss.h                             objs/lib/nginx-vod-module/ngx_http_vod_mss_commands.h                    objs/lib/nginx-vod-module/ngx_http_vod_mss_conf.h                        objs/lib/nginx-vod-module/ngx_http_vod_request_parse.h                   objs/lib/nginx-vod-module/ngx_http_vod_status.h                          objs/lib/nginx-vod-module/ngx_http_vod_submodule.h                       objs/lib/nginx-vod-module/ngx_http_vod_utils.h                           objs/lib/nginx-vod-module/ngx_perf_counters.h                            objs/lib/nginx-vod-module/ngx_perf_counters_x.h                          objs/lib/nginx-vod-module/vod/aes_defs.h                                 objs/lib/nginx-vod-module/vod/avc_defs.h                                 objs/lib/nginx-vod-module/vod/avc_parser.h                               objs/lib/nginx-vod-module/vod/avc_hevc_parser.h                          objs/lib/nginx-vod-module/vod/bit_read_stream.h                          objs/lib/nginx-vod-module/vod/buffer_pool.h                              objs/lib/nginx-vod-module/vod/codec_config.h                             objs/lib/nginx-vod-module/vod/common.h                                   objs/lib/nginx-vod-module/vod/dash/dash_packager.h                       objs/lib/nginx-vod-module/vod/dynamic_buffer.h                           objs/lib/nginx-vod-module/vod/filters/audio_filter.h                     objs/lib/nginx-vod-module/vod/filters/concat_clip.h                      objs/lib/nginx-vod-module/vod/filters/dynamic_clip.h                     objs/lib/nginx-vod-module/vod/filters/filter.h                           objs/lib/nginx-vod-module/vod/filters/gain_filter.h                      objs/lib/nginx-vod-module/vod/filters/mix_filter.h                       objs/lib/nginx-vod-module/vod/filters/rate_filter.h                      objs/lib/nginx-vod-module/vod/hds/hds_amf0_encoder.h                     objs/lib/nginx-vod-module/vod/hds/hds_amf0_fields_x.h                    objs/lib/nginx-vod-module/vod/hds/hds_encryption.h                       objs/lib/nginx-vod-module/vod/hds/hds_fragment.h                         objs/lib/nginx-vod-module/vod/hds/hds_manifest.h                         objs/lib/nginx-vod-module/vod/hevc_parser.h                              objs/lib/nginx-vod-module/vod/hls/adts_encoder_filter.h                  objs/lib/nginx-vod-module/vod/hls/bit_fields.h                           objs/lib/nginx-vod-module/vod/hls/buffer_filter.h                        objs/lib/nginx-vod-module/vod/hls/frame_joiner_filter.h                  objs/lib/nginx-vod-module/vod/hls/hls_encryption.h                       objs/lib/nginx-vod-module/vod/hls/hls_muxer.h                            objs/lib/nginx-vod-module/vod/hls/id3_encoder_filter.h                   objs/lib/nginx-vod-module/vod/hls/m3u8_builder.h                         objs/lib/nginx-vod-module/vod/hls/media_filter.h                         objs/lib/nginx-vod-module/vod/hls/mp4_to_annexb_filter.h                 objs/lib/nginx-vod-module/vod/hls/mpegts_encoder_filter.h                objs/lib/nginx-vod-module/vod/input/silence_generator.h                  objs/lib/nginx-vod-module/vod/input/frames_source.h                      objs/lib/nginx-vod-module/vod/input/frames_source_cache.h                objs/lib/nginx-vod-module/vod/input/frames_source_memory.h               objs/lib/nginx-vod-module/vod/input/read_cache.h                         objs/lib/nginx-vod-module/vod/json_parser.h                              objs/lib/nginx-vod-module/vod/language_code.h                            objs/lib/nginx-vod-module/vod/languages_hash_params.h                    objs/lib/nginx-vod-module/vod/languages_x.h                              objs/lib/nginx-vod-module/vod/manifest_utils.h                           objs/lib/nginx-vod-module/vod/media_clip.h                               objs/lib/nginx-vod-module/vod/media_format.h                             objs/lib/nginx-vod-module/vod/media_set.h                                objs/lib/nginx-vod-module/vod/media_set_parser.h                         objs/lib/nginx-vod-module/vod/mkv/ebml.h                                 objs/lib/nginx-vod-module/vod/mkv/mkv_builder.h                          objs/lib/nginx-vod-module/vod/mkv/mkv_defs.h                             objs/lib/nginx-vod-module/vod/mkv/mkv_format.h                           objs/lib/nginx-vod-module/vod/mp4/mp4_defs.h                             objs/lib/nginx-vod-module/vod/mp4/mp4_format.h                           objs/lib/nginx-vod-module/vod/mp4/mp4_fragment.h                         objs/lib/nginx-vod-module/vod/mp4/mp4_init_segment.h                     objs/lib/nginx-vod-module/vod/mp4/mp4_muxer.h                            objs/lib/nginx-vod-module/vod/mp4/mp4_parser.h                           objs/lib/nginx-vod-module/vod/mp4/mp4_clipper.h              objs/lib/nginx-vod-module/vod/mp4/mp4_parser_base.h                      objs/lib/nginx-vod-module/vod/mp4/mp4_write_stream.h                     objs/lib/nginx-vod-module/vod/mss/mss_packager.h                         objs/lib/nginx-vod-module/vod/subtitle/cap_format.h                      objs/lib/nginx-vod-module/vod/subtitle/dfxp_format.h                     objs/lib/nginx-vod-module/vod/subtitle/subtitle_format.h                 objs/lib/nginx-vod-module/vod/subtitle/ttml_builder.h                    objs/lib/nginx-vod-module/vod/subtitle/webvtt_builder.h                  objs/lib/nginx-vod-module/vod/subtitle/webvtt_format.h                   objs/lib/nginx-vod-module/vod/subtitle/webvtt_format_template.h           objs/lib/nginx-vod-module/vod/parse_utils.h                              objs/lib/nginx-vod-module/vod/read_stream.h                              objs/lib/nginx-vod-module/vod/segmenter.h                                objs/lib/nginx-vod-module/vod/udrm.h                                     objs/lib/nginx-vod-module/vod/write_buffer.h                             objs/lib/nginx-vod-module/vod/write_buffer_queue.h                       objs/lib/nginx-vod-module/vod/write_stream.h                              $(HTTP_DEPS)


build:	binary modules manpage

binary:	objs/nginx.exe

objs/nginx.exe:	objs/src/core/nginx.obj \
	objs/src/core/ngx_log.obj \
	objs/src/core/ngx_palloc.obj \
	objs/src/core/ngx_array.obj \
	objs/src/core/ngx_list.obj \
	objs/src/core/ngx_hash.obj \
	objs/src/core/ngx_buf.obj \
	objs/src/core/ngx_queue.obj \
	objs/src/core/ngx_output_chain.obj \
	objs/src/core/ngx_string.obj \
	objs/src/core/ngx_parse.obj \
	objs/src/core/ngx_parse_time.obj \
	objs/src/core/ngx_inet.obj \
	objs/src/core/ngx_file.obj \
	objs/src/core/ngx_crc32.obj \
	objs/src/core/ngx_murmurhash.obj \
	objs/src/core/ngx_md5.obj \
	objs/src/core/ngx_sha1.obj \
	objs/src/core/ngx_rbtree.obj \
	objs/src/core/ngx_radix_tree.obj \
	objs/src/core/ngx_slab.obj \
	objs/src/core/ngx_times.obj \
	objs/src/core/ngx_shmtx.obj \
	objs/src/core/ngx_connection.obj \
	objs/src/core/ngx_cycle.obj \
	objs/src/core/ngx_spinlock.obj \
	objs/src/core/ngx_rwlock.obj \
	objs/src/core/ngx_cpuinfo.obj \
	objs/src/core/ngx_conf_file.obj \
	objs/src/core/ngx_module.obj \
	objs/src/core/ngx_resolver.obj \
	objs/src/core/ngx_open_file_cache.obj \
	objs/src/core/ngx_crypt.obj \
	objs/src/core/ngx_proxy_protocol.obj \
	objs/src/core/ngx_syslog.obj \
	objs/src/event/ngx_event.obj \
	objs/src/event/ngx_event_timer.obj \
	objs/src/event/ngx_event_posted.obj \
	objs/src/event/ngx_event_accept.obj \
	objs/src/event/ngx_event_connect.obj \
	objs/src/event/ngx_event_pipe.obj \
	objs/src/os/win32/ngx_errno.obj \
	objs/src/os/win32/ngx_alloc.obj \
	objs/src/os/win32/ngx_files.obj \
	objs/src/os/win32/ngx_shmem.obj \
	objs/src/os/win32/ngx_time.obj \
	objs/src/os/win32/ngx_process.obj \
	objs/src/os/win32/ngx_thread.obj \
	objs/src/os/win32/ngx_socket.obj \
	objs/src/os/win32/ngx_wsarecv.obj \
	objs/src/os/win32/ngx_wsarecv_chain.obj \
	objs/src/os/win32/ngx_udp_wsarecv.obj \
	objs/src/os/win32/ngx_wsasend.obj \
	objs/src/os/win32/ngx_wsasend_chain.obj \
	objs/src/os/win32/ngx_win32_init.obj \
	objs/src/os/win32/ngx_user.obj \
	objs/src/os/win32/ngx_dlopen.obj \
	objs/src/os/win32/ngx_event_log.obj \
	objs/src/os/win32/ngx_process_cycle.obj \
	objs/src/event/ngx_event_acceptex.obj \
	objs/src/event/modules/ngx_iocp_module.obj \
	objs/src/event/modules/ngx_win32_select_module.obj \
	objs/src/event/ngx_event_openssl.obj \
	objs/src/event/ngx_event_openssl_stapling.obj \
	objs/src/core/ngx_regex.obj \
	objs/src/http/ngx_http.obj \
	objs/src/http/ngx_http_core_module.obj \
	objs/src/http/ngx_http_special_response.obj \
	objs/src/http/ngx_http_request.obj \
	objs/src/http/ngx_http_parse.obj \
	objs/src/http/modules/ngx_http_log_module.obj \
	objs/src/http/ngx_http_request_body.obj \
	objs/src/http/ngx_http_variables.obj \
	objs/src/http/ngx_http_script.obj \
	objs/src/http/ngx_http_upstream.obj \
	objs/src/http/ngx_http_upstream_round_robin.obj \
	objs/src/http/ngx_http_file_cache.obj \
	objs/src/http/ngx_http_write_filter_module.obj \
	objs/src/http/ngx_http_header_filter_module.obj \
	objs/src/http/modules/ngx_http_chunked_filter_module.obj \
	objs/src/http/modules/ngx_http_range_filter_module.obj \
	objs/src/http/modules/ngx_http_gzip_filter_module.obj \
	objs/src/http/ngx_http_postpone_filter_module.obj \
	objs/src/http/modules/ngx_http_ssi_filter_module.obj \
	objs/src/http/modules/ngx_http_charset_filter_module.obj \
	objs/src/http/modules/ngx_http_userid_filter_module.obj \
	objs/src/http/modules/ngx_http_headers_filter_module.obj \
	objs/src/http/ngx_http_copy_filter_module.obj \
	objs/src/http/modules/ngx_http_not_modified_filter_module.obj \
	objs/src/http/modules/ngx_http_static_module.obj \
	objs/src/http/modules/ngx_http_autoindex_module.obj \
	objs/src/http/modules/ngx_http_index_module.obj \
	objs/src/http/modules/ngx_http_mirror_module.obj \
	objs/src/http/modules/ngx_http_try_files_module.obj \
	objs/src/http/modules/ngx_http_auth_basic_module.obj \
	objs/src/http/modules/ngx_http_access_module.obj \
	objs/src/http/modules/ngx_http_limit_conn_module.obj \
	objs/src/http/modules/ngx_http_limit_req_module.obj \
	objs/src/http/modules/ngx_http_geo_module.obj \
	objs/src/http/modules/ngx_http_map_module.obj \
	objs/src/http/modules/ngx_http_split_clients_module.obj \
	objs/src/http/modules/ngx_http_referer_module.obj \
	objs/src/http/modules/ngx_http_rewrite_module.obj \
	objs/src/http/modules/ngx_http_ssl_module.obj \
	objs/src/http/modules/ngx_http_proxy_module.obj \
	objs/src/http/modules/ngx_http_fastcgi_module.obj \
	objs/src/http/modules/ngx_http_uwsgi_module.obj \
	objs/src/http/modules/ngx_http_scgi_module.obj \
	objs/src/http/modules/ngx_http_memcached_module.obj \
	objs/src/http/modules/ngx_http_empty_gif_module.obj \
	objs/src/http/modules/ngx_http_browser_module.obj \
	objs/src/http/modules/ngx_http_upstream_hash_module.obj \
	objs/src/http/modules/ngx_http_upstream_ip_hash_module.obj \
	objs/src/http/modules/ngx_http_upstream_least_conn_module.obj \
	objs/src/http/modules/ngx_http_upstream_keepalive_module.obj \
	objs/src/http/modules/ngx_http_upstream_zone_module.obj \
	objs/addon/dash/edash_packager.obj \
	objs/addon/hls/aes_cbc_encrypt.obj \
	objs/addon/hls/eac3_encrypt_filter.obj \
	objs/addon/hls/frame_encrypt_filter.obj \
	objs/addon/hls/sample_aes_avc_filter.obj \
	objs/addon/mp4/mp4_aes_ctr.obj \
	objs/addon/mp4/mp4_cbcs_encrypt.obj \
	objs/addon/mp4/mp4_cenc_decrypt.obj \
	objs/addon/mp4/mp4_cenc_encrypt.obj \
	objs/addon/mp4/mp4_cenc_passthrough.obj \
	objs/addon/mss/mss_playready.obj \
	objs/addon/nginx-vod-module/ngx_async_open_file_cache.obj \
	objs/addon/nginx-vod-module/ngx_buffer_cache.obj \
	objs/addon/nginx-vod-module/ngx_child_http_request.obj \
	objs/addon/nginx-vod-module/ngx_file_reader.obj \
	objs/addon/nginx-vod-module/ngx_http_vod_conf.obj \
	objs/addon/nginx-vod-module/ngx_http_vod_dash.obj \
	objs/addon/nginx-vod-module/ngx_http_vod_hds.obj \
	objs/addon/nginx-vod-module/ngx_http_vod_hls.obj \
	objs/addon/nginx-vod-module/ngx_http_vod_module.obj \
	objs/addon/nginx-vod-module/ngx_http_vod_mss.obj \
	objs/addon/nginx-vod-module/ngx_http_vod_request_parse.obj \
	objs/addon/nginx-vod-module/ngx_http_vod_status.obj \
	objs/addon/nginx-vod-module/ngx_http_vod_submodule.obj \
	objs/addon/nginx-vod-module/ngx_http_vod_utils.obj \
	objs/addon/nginx-vod-module/ngx_perf_counters.obj \
	objs/addon/vod/avc_parser.obj \
	objs/addon/vod/avc_hevc_parser.obj \
	objs/addon/vod/buffer_pool.obj \
	objs/addon/vod/codec_config.obj \
	objs/addon/vod/common.obj \
	objs/addon/dash/dash_packager.obj \
	objs/addon/vod/dynamic_buffer.obj \
	objs/addon/filters/audio_filter.obj \
	objs/addon/filters/concat_clip.obj \
	objs/addon/filters/dynamic_clip.obj \
	objs/addon/filters/filter.obj \
	objs/addon/filters/gain_filter.obj \
	objs/addon/filters/mix_filter.obj \
	objs/addon/filters/rate_filter.obj \
	objs/addon/hds/hds_amf0_encoder.obj \
	objs/addon/hds/hds_fragment.obj \
	objs/addon/hds/hds_manifest.obj \
	objs/addon/vod/hevc_parser.obj \
	objs/addon/hls/adts_encoder_filter.obj \
	objs/addon/hls/buffer_filter.obj \
	objs/addon/hls/frame_joiner_filter.obj \
	objs/addon/hls/hls_muxer.obj \
	objs/addon/hls/id3_encoder_filter.obj \
	objs/addon/hls/m3u8_builder.obj \
	objs/addon/hls/mp4_to_annexb_filter.obj \
	objs/addon/hls/mpegts_encoder_filter.obj \
	objs/addon/input/silence_generator.obj \
	objs/addon/input/frames_source_cache.obj \
	objs/addon/input/frames_source_memory.obj \
	objs/addon/input/read_cache.obj \
	objs/addon/vod/json_parser.obj \
	objs/addon/vod/language_code.obj \
	objs/addon/vod/manifest_utils.obj \
	objs/addon/vod/media_format.obj \
	objs/addon/vod/media_set_parser.obj \
	objs/addon/mkv/ebml.obj \
	objs/addon/mkv/mkv_builder.obj \
	objs/addon/mkv/mkv_defs.obj \
	objs/addon/mkv/mkv_format.obj \
	objs/addon/mp4/mp4_format.obj \
	objs/addon/mp4/mp4_fragment.obj \
	objs/addon/mp4/mp4_init_segment.obj \
	objs/addon/mp4/mp4_muxer.obj \
	objs/addon/mp4/mp4_parser.obj \
	objs/addon/mp4/mp4_clipper.obj \
	objs/addon/mp4/mp4_parser_base.obj \
	objs/addon/mss/mss_packager.obj \
	objs/addon/subtitle/cap_format.obj \
	objs/addon/subtitle/subtitle_format.obj \
	objs/addon/subtitle/ttml_builder.obj \
	objs/addon/subtitle/webvtt_builder.obj \
	objs/addon/subtitle/webvtt_format.obj \
	objs/addon/vod/parse_utils.obj \
	objs/addon/vod/segmenter.obj \
	objs/addon/vod/udrm.obj \
	objs/addon/vod/write_buffer.obj \
	objs/addon/vod/write_buffer_queue.obj \
	objs/ngx_modules.obj \
	objs/nginx.res \
	objs/lib/pcre-8.40/pcre.lib \
	objs/lib/zlib/zlib.lib
	$(LINK) @<<
	-Feobjs/nginx
	objs/src/core/nginx.obj 
	objs/src/core/ngx_log.obj 
	objs/src/core/ngx_palloc.obj 
	objs/src/core/ngx_array.obj 
	objs/src/core/ngx_list.obj 
	objs/src/core/ngx_hash.obj 
	objs/src/core/ngx_buf.obj 
	objs/src/core/ngx_queue.obj 
	objs/src/core/ngx_output_chain.obj 
	objs/src/core/ngx_string.obj 
	objs/src/core/ngx_parse.obj 
	objs/src/core/ngx_parse_time.obj 
	objs/src/core/ngx_inet.obj 
	objs/src/core/ngx_file.obj 
	objs/src/core/ngx_crc32.obj 
	objs/src/core/ngx_murmurhash.obj 
	objs/src/core/ngx_md5.obj 
	objs/src/core/ngx_sha1.obj 
	objs/src/core/ngx_rbtree.obj 
	objs/src/core/ngx_radix_tree.obj 
	objs/src/core/ngx_slab.obj 
	objs/src/core/ngx_times.obj 
	objs/src/core/ngx_shmtx.obj 
	objs/src/core/ngx_connection.obj 
	objs/src/core/ngx_cycle.obj 
	objs/src/core/ngx_spinlock.obj 
	objs/src/core/ngx_rwlock.obj 
	objs/src/core/ngx_cpuinfo.obj 
	objs/src/core/ngx_conf_file.obj 
	objs/src/core/ngx_module.obj 
	objs/src/core/ngx_resolver.obj 
	objs/src/core/ngx_open_file_cache.obj 
	objs/src/core/ngx_crypt.obj 
	objs/src/core/ngx_proxy_protocol.obj 
	objs/src/core/ngx_syslog.obj 
	objs/src/event/ngx_event.obj 
	objs/src/event/ngx_event_timer.obj 
	objs/src/event/ngx_event_posted.obj 
	objs/src/event/ngx_event_accept.obj 
	objs/src/event/ngx_event_connect.obj 
	objs/src/event/ngx_event_pipe.obj 
	objs/src/os/win32/ngx_errno.obj 
	objs/src/os/win32/ngx_alloc.obj 
	objs/src/os/win32/ngx_files.obj 
	objs/src/os/win32/ngx_shmem.obj 
	objs/src/os/win32/ngx_time.obj 
	objs/src/os/win32/ngx_process.obj 
	objs/src/os/win32/ngx_thread.obj 
	objs/src/os/win32/ngx_socket.obj 
	objs/src/os/win32/ngx_wsarecv.obj 
	objs/src/os/win32/ngx_wsarecv_chain.obj 
	objs/src/os/win32/ngx_udp_wsarecv.obj 
	objs/src/os/win32/ngx_wsasend.obj 
	objs/src/os/win32/ngx_wsasend_chain.obj 
	objs/src/os/win32/ngx_win32_init.obj 
	objs/src/os/win32/ngx_user.obj 
	objs/src/os/win32/ngx_dlopen.obj 
	objs/src/os/win32/ngx_event_log.obj 
	objs/src/os/win32/ngx_process_cycle.obj 
	objs/src/event/ngx_event_acceptex.obj 
	objs/src/event/modules/ngx_iocp_module.obj 
	objs/src/event/modules/ngx_win32_select_module.obj 
	objs/src/event/ngx_event_openssl.obj 
	objs/src/event/ngx_event_openssl_stapling.obj 
	objs/src/core/ngx_regex.obj 
	objs/src/http/ngx_http.obj 
	objs/src/http/ngx_http_core_module.obj 
	objs/src/http/ngx_http_special_response.obj 
	objs/src/http/ngx_http_request.obj 
	objs/src/http/ngx_http_parse.obj 
	objs/src/http/modules/ngx_http_log_module.obj 
	objs/src/http/ngx_http_request_body.obj 
	objs/src/http/ngx_http_variables.obj 
	objs/src/http/ngx_http_script.obj 
	objs/src/http/ngx_http_upstream.obj 
	objs/src/http/ngx_http_upstream_round_robin.obj 
	objs/src/http/ngx_http_file_cache.obj 
	objs/src/http/ngx_http_write_filter_module.obj 
	objs/src/http/ngx_http_header_filter_module.obj 
	objs/src/http/modules/ngx_http_chunked_filter_module.obj 
	objs/src/http/modules/ngx_http_range_filter_module.obj 
	objs/src/http/modules/ngx_http_gzip_filter_module.obj 
	objs/src/http/ngx_http_postpone_filter_module.obj 
	objs/src/http/modules/ngx_http_ssi_filter_module.obj 
	objs/src/http/modules/ngx_http_charset_filter_module.obj 
	objs/src/http/modules/ngx_http_userid_filter_module.obj 
	objs/src/http/modules/ngx_http_headers_filter_module.obj 
	objs/src/http/ngx_http_copy_filter_module.obj 
	objs/src/http/modules/ngx_http_not_modified_filter_module.obj 
	objs/src/http/modules/ngx_http_static_module.obj 
	objs/src/http/modules/ngx_http_autoindex_module.obj 
	objs/src/http/modules/ngx_http_index_module.obj 
	objs/src/http/modules/ngx_http_mirror_module.obj 
	objs/src/http/modules/ngx_http_try_files_module.obj 
	objs/src/http/modules/ngx_http_auth_basic_module.obj 
	objs/src/http/modules/ngx_http_access_module.obj 
	objs/src/http/modules/ngx_http_limit_conn_module.obj 
	objs/src/http/modules/ngx_http_limit_req_module.obj 
	objs/src/http/modules/ngx_http_geo_module.obj 
	objs/src/http/modules/ngx_http_map_module.obj 
	objs/src/http/modules/ngx_http_split_clients_module.obj 
	objs/src/http/modules/ngx_http_referer_module.obj 
	objs/src/http/modules/ngx_http_rewrite_module.obj 
	objs/src/http/modules/ngx_http_ssl_module.obj 
	objs/src/http/modules/ngx_http_proxy_module.obj 
	objs/src/http/modules/ngx_http_fastcgi_module.obj 
	objs/src/http/modules/ngx_http_uwsgi_module.obj 
	objs/src/http/modules/ngx_http_scgi_module.obj 
	objs/src/http/modules/ngx_http_memcached_module.obj 
	objs/src/http/modules/ngx_http_empty_gif_module.obj 
	objs/src/http/modules/ngx_http_browser_module.obj 
	objs/src/http/modules/ngx_http_upstream_hash_module.obj 
	objs/src/http/modules/ngx_http_upstream_ip_hash_module.obj 
	objs/src/http/modules/ngx_http_upstream_least_conn_module.obj 
	objs/src/http/modules/ngx_http_upstream_keepalive_module.obj 
	objs/src/http/modules/ngx_http_upstream_zone_module.obj 
	objs/addon/dash/edash_packager.obj 
	objs/addon/hls/aes_cbc_encrypt.obj 
	objs/addon/hls/eac3_encrypt_filter.obj 
	objs/addon/hls/frame_encrypt_filter.obj 
	objs/addon/hls/sample_aes_avc_filter.obj 
	objs/addon/mp4/mp4_aes_ctr.obj 
	objs/addon/mp4/mp4_cbcs_encrypt.obj 
	objs/addon/mp4/mp4_cenc_decrypt.obj 
	objs/addon/mp4/mp4_cenc_encrypt.obj 
	objs/addon/mp4/mp4_cenc_passthrough.obj 
	objs/addon/mss/mss_playready.obj 
	objs/addon/nginx-vod-module/ngx_async_open_file_cache.obj 
	objs/addon/nginx-vod-module/ngx_buffer_cache.obj 
	objs/addon/nginx-vod-module/ngx_child_http_request.obj 
	objs/addon/nginx-vod-module/ngx_file_reader.obj 
	objs/addon/nginx-vod-module/ngx_http_vod_conf.obj 
	objs/addon/nginx-vod-module/ngx_http_vod_dash.obj 
	objs/addon/nginx-vod-module/ngx_http_vod_hds.obj 
	objs/addon/nginx-vod-module/ngx_http_vod_hls.obj 
	objs/addon/nginx-vod-module/ngx_http_vod_module.obj 
	objs/addon/nginx-vod-module/ngx_http_vod_mss.obj 
	objs/addon/nginx-vod-module/ngx_http_vod_request_parse.obj 
	objs/addon/nginx-vod-module/ngx_http_vod_status.obj 
	objs/addon/nginx-vod-module/ngx_http_vod_submodule.obj 
	objs/addon/nginx-vod-module/ngx_http_vod_utils.obj 
	objs/addon/nginx-vod-module/ngx_perf_counters.obj 
	objs/addon/vod/avc_parser.obj 
	objs/addon/vod/avc_hevc_parser.obj 
	objs/addon/vod/buffer_pool.obj 
	objs/addon/vod/codec_config.obj 
	objs/addon/vod/common.obj 
	objs/addon/dash/dash_packager.obj 
	objs/addon/vod/dynamic_buffer.obj 
	objs/addon/filters/audio_filter.obj 
	objs/addon/filters/concat_clip.obj 
	objs/addon/filters/dynamic_clip.obj 
	objs/addon/filters/filter.obj 
	objs/addon/filters/gain_filter.obj 
	objs/addon/filters/mix_filter.obj 
	objs/addon/filters/rate_filter.obj 
	objs/addon/hds/hds_amf0_encoder.obj 
	objs/addon/hds/hds_fragment.obj 
	objs/addon/hds/hds_manifest.obj 
	objs/addon/vod/hevc_parser.obj 
	objs/addon/hls/adts_encoder_filter.obj 
	objs/addon/hls/buffer_filter.obj 
	objs/addon/hls/frame_joiner_filter.obj 
	objs/addon/hls/hls_muxer.obj 
	objs/addon/hls/id3_encoder_filter.obj 
	objs/addon/hls/m3u8_builder.obj 
	objs/addon/hls/mp4_to_annexb_filter.obj 
	objs/addon/hls/mpegts_encoder_filter.obj 
	objs/addon/input/silence_generator.obj 
	objs/addon/input/frames_source_cache.obj 
	objs/addon/input/frames_source_memory.obj 
	objs/addon/input/read_cache.obj 
	objs/addon/vod/json_parser.obj 
	objs/addon/vod/language_code.obj 
	objs/addon/vod/manifest_utils.obj 
	objs/addon/vod/media_format.obj 
	objs/addon/vod/media_set_parser.obj 
	objs/addon/mkv/ebml.obj 
	objs/addon/mkv/mkv_builder.obj 
	objs/addon/mkv/mkv_defs.obj 
	objs/addon/mkv/mkv_format.obj 
	objs/addon/mp4/mp4_format.obj 
	objs/addon/mp4/mp4_fragment.obj 
	objs/addon/mp4/mp4_init_segment.obj 
	objs/addon/mp4/mp4_muxer.obj 
	objs/addon/mp4/mp4_parser.obj 
	objs/addon/mp4/mp4_clipper.obj 
	objs/addon/mp4/mp4_parser_base.obj 
	objs/addon/mss/mss_packager.obj 
	objs/addon/subtitle/cap_format.obj 
	objs/addon/subtitle/subtitle_format.obj 
	objs/addon/subtitle/ttml_builder.obj 
	objs/addon/subtitle/webvtt_builder.obj 
	objs/addon/subtitle/webvtt_format.obj 
	objs/addon/vod/parse_utils.obj 
	objs/addon/vod/segmenter.obj 
	objs/addon/vod/udrm.obj 
	objs/addon/vod/write_buffer.obj 
	objs/addon/vod/write_buffer_queue.obj 
	objs/ngx_modules.obj 
	kernel32.lib user32.lib advapi32.lib ws2_32.lib objs/lib/pcre-8.40/pcre.lib objs/lib/openssl/openssl/lib/ssleay32.lib objs/lib/openssl/openssl/lib/libeay32.lib gdi32.lib crypt32.lib objs/lib/zlib/zlib.lib 
	objs/nginx.res -link -verbose:lib -debug objs/ngx_pch.obj
	
<<

modules:

objs/ngx_modules.obj:	$(CORE_DEPS) \
	objs/ngx_modules.c
	$(CC) -c $(CFLAGS) -Yungx_config.h -Fpobjs/ngx_config.pch $(ALL_INCS) \
		-Foobjs/ngx_modules.obj \
		objs/ngx_modules.c


objs/src/core/nginx.obj:	$(CORE_DEPS) \
	src/core/nginx.c
	$(CC) -c $(CFLAGS) -Yungx_config.h -Fpobjs/ngx_config.pch $(ALL_INCS) \
		-Foobjs/src/core/nginx.obj \
		src/core/nginx.c


objs/src/core/ngx_log.obj:	$(CORE_DEPS) \
	src/core/ngx_log.c
	$(CC) -c $(CFLAGS) -Yungx_config.h -Fpobjs/ngx_config.pch $(ALL_INCS) \
		-Foobjs/src/core/ngx_log.obj \
		src/core/ngx_log.c


objs/src/core/ngx_palloc.obj:	$(CORE_DEPS) \
	src/core/ngx_palloc.c
	$(CC) -c $(CFLAGS) -Yungx_config.h -Fpobjs/ngx_config.pch $(ALL_INCS) \
		-Foobjs/src/core/ngx_palloc.obj \
		src/core/ngx_palloc.c


objs/src/core/ngx_array.obj:	$(CORE_DEPS) \
	src/core/ngx_array.c
	$(CC) -c $(CFLAGS) -Yungx_config.h -Fpobjs/ngx_config.pch $(ALL_INCS) \
		-Foobjs/src/core/ngx_array.obj \
		src/core/ngx_array.c


objs/src/core/ngx_list.obj:	$(CORE_DEPS) \
	src/core/ngx_list.c
	$(CC) -c $(CFLAGS) -Yungx_config.h -Fpobjs/ngx_config.pch $(ALL_INCS) \
		-Foobjs/src/core/ngx_list.obj \
		src/core/ngx_list.c


objs/src/core/ngx_hash.obj:	$(CORE_DEPS) \
	src/core/ngx_hash.c
	$(CC) -c $(CFLAGS) -Yungx_config.h -Fpobjs/ngx_config.pch $(ALL_INCS) \
		-Foobjs/src/core/ngx_hash.obj \
		src/core/ngx_hash.c


objs/src/core/ngx_buf.obj:	$(CORE_DEPS) \
	src/core/ngx_buf.c
	$(CC) -c $(CFLAGS) -Yungx_config.h -Fpobjs/ngx_config.pch $(ALL_INCS) \
		-Foobjs/src/core/ngx_buf.obj \
		src/core/ngx_buf.c


objs/src/core/ngx_queue.obj:	$(CORE_DEPS) \
	src/core/ngx_queue.c
	$(CC) -c $(CFLAGS) -Yungx_config.h -Fpobjs/ngx_config.pch $(ALL_INCS) \
		-Foobjs/src/core/ngx_queue.obj \
		src/core/ngx_queue.c


objs/src/core/ngx_output_chain.obj:	$(CORE_DEPS) \
	src/core/ngx_output_chain.c
	$(CC) -c $(CFLAGS) -Yungx_config.h -Fpobjs/ngx_config.pch $(ALL_INCS) \
		-Foobjs/src/core/ngx_output_chain.obj \
		src/core/ngx_output_chain.c


objs/src/core/ngx_string.obj:	$(CORE_DEPS) \
	src/core/ngx_string.c
	$(CC) -c $(CFLAGS) -Yungx_config.h -Fpobjs/ngx_config.pch $(ALL_INCS) \
		-Foobjs/src/core/ngx_string.obj \
		src/core/ngx_string.c


objs/src/core/ngx_parse.obj:	$(CORE_DEPS) \
	src/core/ngx_parse.c
	$(CC) -c $(CFLAGS) -Yungx_config.h -Fpobjs/ngx_config.pch $(ALL_INCS) \
		-Foobjs/src/core/ngx_parse.obj \
		src/core/ngx_parse.c


objs/src/core/ngx_parse_time.obj:	$(CORE_DEPS) \
	src/core/ngx_parse_time.c
	$(CC) -c $(CFLAGS) -Yungx_config.h -Fpobjs/ngx_config.pch $(ALL_INCS) \
		-Foobjs/src/core/ngx_parse_time.obj \
		src/core/ngx_parse_time.c


objs/src/core/ngx_inet.obj:	$(CORE_DEPS) \
	src/core/ngx_inet.c
	$(CC) -c $(CFLAGS) -Yungx_config.h -Fpobjs/ngx_config.pch $(ALL_INCS) \
		-Foobjs/src/core/ngx_inet.obj \
		src/core/ngx_inet.c


objs/src/core/ngx_file.obj:	$(CORE_DEPS) \
	src/core/ngx_file.c
	$(CC) -c $(CFLAGS) -Yungx_config.h -Fpobjs/ngx_config.pch $(ALL_INCS) \
		-Foobjs/src/core/ngx_file.obj \
		src/core/ngx_file.c


objs/src/core/ngx_crc32.obj:	$(CORE_DEPS) \
	src/core/ngx_crc32.c
	$(CC) -c $(CFLAGS) -Yungx_config.h -Fpobjs/ngx_config.pch $(ALL_INCS) \
		-Foobjs/src/core/ngx_crc32.obj \
		src/core/ngx_crc32.c


objs/src/core/ngx_murmurhash.obj:	$(CORE_DEPS) \
	src/core/ngx_murmurhash.c
	$(CC) -c $(CFLAGS) -Yungx_config.h -Fpobjs/ngx_config.pch $(ALL_INCS) \
		-Foobjs/src/core/ngx_murmurhash.obj \
		src/core/ngx_murmurhash.c


objs/src/core/ngx_md5.obj:	$(CORE_DEPS) \
	src/core/ngx_md5.c
	$(CC) -c $(CFLAGS) -Yungx_config.h -Fpobjs/ngx_config.pch $(ALL_INCS) \
		-Foobjs/src/core/ngx_md5.obj \
		src/core/ngx_md5.c


objs/src/core/ngx_sha1.obj:	$(CORE_DEPS) \
	src/core/ngx_sha1.c
	$(CC) -c $(CFLAGS) -Yungx_config.h -Fpobjs/ngx_config.pch $(ALL_INCS) \
		-Foobjs/src/core/ngx_sha1.obj \
		src/core/ngx_sha1.c


objs/src/core/ngx_rbtree.obj:	$(CORE_DEPS) \
	src/core/ngx_rbtree.c
	$(CC) -c $(CFLAGS) -Yungx_config.h -Fpobjs/ngx_config.pch $(ALL_INCS) \
		-Foobjs/src/core/ngx_rbtree.obj \
		src/core/ngx_rbtree.c


objs/src/core/ngx_radix_tree.obj:	$(CORE_DEPS) \
	src/core/ngx_radix_tree.c
	$(CC) -c $(CFLAGS) -Yungx_config.h -Fpobjs/ngx_config.pch $(ALL_INCS) \
		-Foobjs/src/core/ngx_radix_tree.obj \
		src/core/ngx_radix_tree.c


objs/src/core/ngx_slab.obj:	$(CORE_DEPS) \
	src/core/ngx_slab.c
	$(CC) -c $(CFLAGS) -Yungx_config.h -Fpobjs/ngx_config.pch $(ALL_INCS) \
		-Foobjs/src/core/ngx_slab.obj \
		src/core/ngx_slab.c


objs/src/core/ngx_times.obj:	$(CORE_DEPS) \
	src/core/ngx_times.c
	$(CC) -c $(CFLAGS) -Yungx_config.h -Fpobjs/ngx_config.pch $(ALL_INCS) \
		-Foobjs/src/core/ngx_times.obj \
		src/core/ngx_times.c


objs/src/core/ngx_shmtx.obj:	$(CORE_DEPS) \
	src/core/ngx_shmtx.c
	$(CC) -c $(CFLAGS) -Yungx_config.h -Fpobjs/ngx_config.pch $(ALL_INCS) \
		-Foobjs/src/core/ngx_shmtx.obj \
		src/core/ngx_shmtx.c


objs/src/core/ngx_connection.obj:	$(CORE_DEPS) \
	src/core/ngx_connection.c
	$(CC) -c $(CFLAGS) -Yungx_config.h -Fpobjs/ngx_config.pch $(ALL_INCS) \
		-Foobjs/src/core/ngx_connection.obj \
		src/core/ngx_connection.c


objs/src/core/ngx_cycle.obj:	$(CORE_DEPS) \
	src/core/ngx_cycle.c
	$(CC) -c $(CFLAGS) -Yungx_config.h -Fpobjs/ngx_config.pch $(ALL_INCS) \
		-Foobjs/src/core/ngx_cycle.obj \
		src/core/ngx_cycle.c


objs/src/core/ngx_spinlock.obj:	$(CORE_DEPS) \
	src/core/ngx_spinlock.c
	$(CC) -c $(CFLAGS) -Yungx_config.h -Fpobjs/ngx_config.pch $(ALL_INCS) \
		-Foobjs/src/core/ngx_spinlock.obj \
		src/core/ngx_spinlock.c


objs/src/core/ngx_rwlock.obj:	$(CORE_DEPS) \
	src/core/ngx_rwlock.c
	$(CC) -c $(CFLAGS) -Yungx_config.h -Fpobjs/ngx_config.pch $(ALL_INCS) \
		-Foobjs/src/core/ngx_rwlock.obj \
		src/core/ngx_rwlock.c


objs/src/core/ngx_cpuinfo.obj:	$(CORE_DEPS) \
	src/core/ngx_cpuinfo.c
	$(CC) -c $(CFLAGS) -Yungx_config.h -Fpobjs/ngx_config.pch $(ALL_INCS) \
		-Foobjs/src/core/ngx_cpuinfo.obj \
		src/core/ngx_cpuinfo.c


objs/src/core/ngx_conf_file.obj:	$(CORE_DEPS) \
	src/core/ngx_conf_file.c
	$(CC) -c $(CFLAGS) -Yungx_config.h -Fpobjs/ngx_config.pch $(ALL_INCS) \
		-Foobjs/src/core/ngx_conf_file.obj \
		src/core/ngx_conf_file.c


objs/src/core/ngx_module.obj:	$(CORE_DEPS) \
	src/core/ngx_module.c
	$(CC) -c $(CFLAGS) -Yungx_config.h -Fpobjs/ngx_config.pch $(ALL_INCS) \
		-Foobjs/src/core/ngx_module.obj \
		src/core/ngx_module.c


objs/src/core/ngx_resolver.obj:	$(CORE_DEPS) \
	src/core/ngx_resolver.c
	$(CC) -c $(CFLAGS) -Yungx_config.h -Fpobjs/ngx_config.pch $(ALL_INCS) \
		-Foobjs/src/core/ngx_resolver.obj \
		src/core/ngx_resolver.c


objs/src/core/ngx_open_file_cache.obj:	$(CORE_DEPS) \
	src/core/ngx_open_file_cache.c
	$(CC) -c $(CFLAGS) -Yungx_config.h -Fpobjs/ngx_config.pch $(ALL_INCS) \
		-Foobjs/src/core/ngx_open_file_cache.obj \
		src/core/ngx_open_file_cache.c


objs/src/core/ngx_crypt.obj:	$(CORE_DEPS) \
	src/core/ngx_crypt.c
	$(CC) -c $(CFLAGS) -Yungx_config.h -Fpobjs/ngx_config.pch $(ALL_INCS) \
		-Foobjs/src/core/ngx_crypt.obj \
		src/core/ngx_crypt.c


objs/src/core/ngx_proxy_protocol.obj:	$(CORE_DEPS) \
	src/core/ngx_proxy_protocol.c
	$(CC) -c $(CFLAGS) -Yungx_config.h -Fpobjs/ngx_config.pch $(ALL_INCS) \
		-Foobjs/src/core/ngx_proxy_protocol.obj \
		src/core/ngx_proxy_protocol.c


objs/src/core/ngx_syslog.obj:	$(CORE_DEPS) \
	src/core/ngx_syslog.c
	$(CC) -c $(CFLAGS) -Yungx_config.h -Fpobjs/ngx_config.pch $(ALL_INCS) \
		-Foobjs/src/core/ngx_syslog.obj \
		src/core/ngx_syslog.c


objs/src/event/ngx_event.obj:	$(CORE_DEPS) \
	src/event/ngx_event.c
	$(CC) -c $(CFLAGS) -Yungx_config.h -Fpobjs/ngx_config.pch $(ALL_INCS) \
		-Foobjs/src/event/ngx_event.obj \
		src/event/ngx_event.c


objs/src/event/ngx_event_timer.obj:	$(CORE_DEPS) \
	src/event/ngx_event_timer.c
	$(CC) -c $(CFLAGS) -Yungx_config.h -Fpobjs/ngx_config.pch $(ALL_INCS) \
		-Foobjs/src/event/ngx_event_timer.obj \
		src/event/ngx_event_timer.c


objs/src/event/ngx_event_posted.obj:	$(CORE_DEPS) \
	src/event/ngx_event_posted.c
	$(CC) -c $(CFLAGS) -Yungx_config.h -Fpobjs/ngx_config.pch $(ALL_INCS) \
		-Foobjs/src/event/ngx_event_posted.obj \
		src/event/ngx_event_posted.c


objs/src/event/ngx_event_accept.obj:	$(CORE_DEPS) \
	src/event/ngx_event_accept.c
	$(CC) -c $(CFLAGS) -Yungx_config.h -Fpobjs/ngx_config.pch $(ALL_INCS) \
		-Foobjs/src/event/ngx_event_accept.obj \
		src/event/ngx_event_accept.c


objs/src/event/ngx_event_connect.obj:	$(CORE_DEPS) \
	src/event/ngx_event_connect.c
	$(CC) -c $(CFLAGS) -Yungx_config.h -Fpobjs/ngx_config.pch $(ALL_INCS) \
		-Foobjs/src/event/ngx_event_connect.obj \
		src/event/ngx_event_connect.c


objs/src/event/ngx_event_pipe.obj:	$(CORE_DEPS) \
	src/event/ngx_event_pipe.c
	$(CC) -c $(CFLAGS) -Yungx_config.h -Fpobjs/ngx_config.pch $(ALL_INCS) \
		-Foobjs/src/event/ngx_event_pipe.obj \
		src/event/ngx_event_pipe.c


objs/src/os/win32/ngx_errno.obj:	$(CORE_DEPS) \
	src/os/win32/ngx_errno.c
	$(CC) -c $(CFLAGS) -Yungx_config.h -Fpobjs/ngx_config.pch $(ALL_INCS) \
		-Foobjs/src/os/win32/ngx_errno.obj \
		src/os/win32/ngx_errno.c


objs/src/os/win32/ngx_alloc.obj:	$(CORE_DEPS) \
	src/os/win32/ngx_alloc.c
	$(CC) -c $(CFLAGS) -Yungx_config.h -Fpobjs/ngx_config.pch $(ALL_INCS) \
		-Foobjs/src/os/win32/ngx_alloc.obj \
		src/os/win32/ngx_alloc.c


objs/src/os/win32/ngx_files.obj:	$(CORE_DEPS) \
	src/os/win32/ngx_files.c
	$(CC) -c $(CFLAGS) -Yungx_config.h -Fpobjs/ngx_config.pch $(ALL_INCS) \
		-Foobjs/src/os/win32/ngx_files.obj \
		src/os/win32/ngx_files.c


objs/src/os/win32/ngx_shmem.obj:	$(CORE_DEPS) \
	src/os/win32/ngx_shmem.c
	$(CC) -c $(CFLAGS) -Yungx_config.h -Fpobjs/ngx_config.pch $(ALL_INCS) \
		-Foobjs/src/os/win32/ngx_shmem.obj \
		src/os/win32/ngx_shmem.c


objs/src/os/win32/ngx_time.obj:	$(CORE_DEPS) \
	src/os/win32/ngx_time.c
	$(CC) -c $(CFLAGS) -Yungx_config.h -Fpobjs/ngx_config.pch $(ALL_INCS) \
		-Foobjs/src/os/win32/ngx_time.obj \
		src/os/win32/ngx_time.c


objs/src/os/win32/ngx_process.obj:	$(CORE_DEPS) \
	src/os/win32/ngx_process.c
	$(CC) -c $(CFLAGS) -Yungx_config.h -Fpobjs/ngx_config.pch $(ALL_INCS) \
		-Foobjs/src/os/win32/ngx_process.obj \
		src/os/win32/ngx_process.c


objs/src/os/win32/ngx_thread.obj:	$(CORE_DEPS) \
	src/os/win32/ngx_thread.c
	$(CC) -c $(CFLAGS) -Yungx_config.h -Fpobjs/ngx_config.pch $(ALL_INCS) \
		-Foobjs/src/os/win32/ngx_thread.obj \
		src/os/win32/ngx_thread.c


objs/src/os/win32/ngx_socket.obj:	$(CORE_DEPS) \
	src/os/win32/ngx_socket.c
	$(CC) -c $(CFLAGS) -Yungx_config.h -Fpobjs/ngx_config.pch $(ALL_INCS) \
		-Foobjs/src/os/win32/ngx_socket.obj \
		src/os/win32/ngx_socket.c


objs/src/os/win32/ngx_wsarecv.obj:	$(CORE_DEPS) \
	src/os/win32/ngx_wsarecv.c
	$(CC) -c $(CFLAGS) -Yungx_config.h -Fpobjs/ngx_config.pch $(ALL_INCS) \
		-Foobjs/src/os/win32/ngx_wsarecv.obj \
		src/os/win32/ngx_wsarecv.c


objs/src/os/win32/ngx_wsarecv_chain.obj:	$(CORE_DEPS) \
	src/os/win32/ngx_wsarecv_chain.c
	$(CC) -c $(CFLAGS) -Yungx_config.h -Fpobjs/ngx_config.pch $(ALL_INCS) \
		-Foobjs/src/os/win32/ngx_wsarecv_chain.obj \
		src/os/win32/ngx_wsarecv_chain.c


objs/src/os/win32/ngx_udp_wsarecv.obj:	$(CORE_DEPS) \
	src/os/win32/ngx_udp_wsarecv.c
	$(CC) -c $(CFLAGS) -Yungx_config.h -Fpobjs/ngx_config.pch $(ALL_INCS) \
		-Foobjs/src/os/win32/ngx_udp_wsarecv.obj \
		src/os/win32/ngx_udp_wsarecv.c


objs/src/os/win32/ngx_wsasend.obj:	$(CORE_DEPS) \
	src/os/win32/ngx_wsasend.c
	$(CC) -c $(CFLAGS) -Yungx_config.h -Fpobjs/ngx_config.pch $(ALL_INCS) \
		-Foobjs/src/os/win32/ngx_wsasend.obj \
		src/os/win32/ngx_wsasend.c


objs/src/os/win32/ngx_wsasend_chain.obj:	$(CORE_DEPS) \
	src/os/win32/ngx_wsasend_chain.c
	$(CC) -c $(CFLAGS) -Yungx_config.h -Fpobjs/ngx_config.pch $(ALL_INCS) \
		-Foobjs/src/os/win32/ngx_wsasend_chain.obj \
		src/os/win32/ngx_wsasend_chain.c


objs/src/os/win32/ngx_win32_init.obj:	$(CORE_DEPS) \
	src/os/win32/ngx_win32_init.c
	$(CC) -c $(CFLAGS) -Yungx_config.h -Fpobjs/ngx_config.pch $(ALL_INCS) \
		-Foobjs/src/os/win32/ngx_win32_init.obj \
		src/os/win32/ngx_win32_init.c


objs/src/os/win32/ngx_user.obj:	$(CORE_DEPS) \
	src/os/win32/ngx_user.c
	$(CC) -c $(CFLAGS) -Yungx_config.h -Fpobjs/ngx_config.pch $(ALL_INCS) \
		-Foobjs/src/os/win32/ngx_user.obj \
		src/os/win32/ngx_user.c


objs/src/os/win32/ngx_dlopen.obj:	$(CORE_DEPS) \
	src/os/win32/ngx_dlopen.c
	$(CC) -c $(CFLAGS) -Yungx_config.h -Fpobjs/ngx_config.pch $(ALL_INCS) \
		-Foobjs/src/os/win32/ngx_dlopen.obj \
		src/os/win32/ngx_dlopen.c


objs/src/os/win32/ngx_event_log.obj:	$(CORE_DEPS) \
	src/os/win32/ngx_event_log.c
	$(CC) -c $(CFLAGS) -Yungx_config.h -Fpobjs/ngx_config.pch $(ALL_INCS) \
		-Foobjs/src/os/win32/ngx_event_log.obj \
		src/os/win32/ngx_event_log.c


objs/src/os/win32/ngx_process_cycle.obj:	$(CORE_DEPS) \
	src/os/win32/ngx_process_cycle.c
	$(CC) -c $(CFLAGS) -Yungx_config.h -Fpobjs/ngx_config.pch $(ALL_INCS) \
		-Foobjs/src/os/win32/ngx_process_cycle.obj \
		src/os/win32/ngx_process_cycle.c


objs/src/event/ngx_event_acceptex.obj:	$(CORE_DEPS) \
	src/event/ngx_event_acceptex.c
	$(CC) -c $(CFLAGS) -Yungx_config.h -Fpobjs/ngx_config.pch $(ALL_INCS) \
		-Foobjs/src/event/ngx_event_acceptex.obj \
		src/event/ngx_event_acceptex.c


objs/src/event/modules/ngx_iocp_module.obj:	$(CORE_DEPS) \
	src/event/modules/ngx_iocp_module.c
	$(CC) -c $(CFLAGS) -Yungx_config.h -Fpobjs/ngx_config.pch $(ALL_INCS) \
		-Foobjs/src/event/modules/ngx_iocp_module.obj \
		src/event/modules/ngx_iocp_module.c


objs/src/event/modules/ngx_win32_select_module.obj:	$(CORE_DEPS) \
	src/event/modules/ngx_win32_select_module.c
	$(CC) -c $(CFLAGS) -Yungx_config.h -Fpobjs/ngx_config.pch $(ALL_INCS) \
		-Foobjs/src/event/modules/ngx_win32_select_module.obj \
		src/event/modules/ngx_win32_select_module.c


objs/src/event/ngx_event_openssl.obj:	$(CORE_DEPS) \
	src/event/ngx_event_openssl.c
	$(CC) -c $(CFLAGS) -Yungx_config.h -Fpobjs/ngx_config.pch $(ALL_INCS) \
		-Foobjs/src/event/ngx_event_openssl.obj \
		src/event/ngx_event_openssl.c


objs/src/event/ngx_event_openssl_stapling.obj:	$(CORE_DEPS) \
	src/event/ngx_event_openssl_stapling.c
	$(CC) -c $(CFLAGS) -Yungx_config.h -Fpobjs/ngx_config.pch $(ALL_INCS) \
		-Foobjs/src/event/ngx_event_openssl_stapling.obj \
		src/event/ngx_event_openssl_stapling.c


objs/src/core/ngx_regex.obj:	$(CORE_DEPS) \
	src/core/ngx_regex.c
	$(CC) -c $(CFLAGS) -Yungx_config.h -Fpobjs/ngx_config.pch $(ALL_INCS) \
		-Foobjs/src/core/ngx_regex.obj \
		src/core/ngx_regex.c


objs/src/http/ngx_http.obj:	$(CORE_DEPS) $(HTTP_DEPS) \
	src/http/ngx_http.c
	$(CC) -c $(CFLAGS) -Yungx_config.h -Fpobjs/ngx_config.pch $(ALL_INCS) \
		-Foobjs/src/http/ngx_http.obj \
		src/http/ngx_http.c


objs/src/http/ngx_http_core_module.obj:	$(CORE_DEPS) $(HTTP_DEPS) \
	src/http/ngx_http_core_module.c
	$(CC) -c $(CFLAGS) -Yungx_config.h -Fpobjs/ngx_config.pch $(ALL_INCS) \
		-Foobjs/src/http/ngx_http_core_module.obj \
		src/http/ngx_http_core_module.c


objs/src/http/ngx_http_special_response.obj:	$(CORE_DEPS) $(HTTP_DEPS) \
	src/http/ngx_http_special_response.c
	$(CC) -c $(CFLAGS) -Yungx_config.h -Fpobjs/ngx_config.pch $(ALL_INCS) \
		-Foobjs/src/http/ngx_http_special_response.obj \
		src/http/ngx_http_special_response.c


objs/src/http/ngx_http_request.obj:	$(CORE_DEPS) $(HTTP_DEPS) \
	src/http/ngx_http_request.c
	$(CC) -c $(CFLAGS) -Yungx_config.h -Fpobjs/ngx_config.pch $(ALL_INCS) \
		-Foobjs/src/http/ngx_http_request.obj \
		src/http/ngx_http_request.c


objs/src/http/ngx_http_parse.obj:	$(CORE_DEPS) $(HTTP_DEPS) \
	src/http/ngx_http_parse.c
	$(CC) -c $(CFLAGS) -Yungx_config.h -Fpobjs/ngx_config.pch $(ALL_INCS) \
		-Foobjs/src/http/ngx_http_parse.obj \
		src/http/ngx_http_parse.c


objs/src/http/modules/ngx_http_log_module.obj:	$(CORE_DEPS) $(HTTP_DEPS) \
	src/http/modules/ngx_http_log_module.c
	$(CC) -c $(CFLAGS) -Yungx_config.h -Fpobjs/ngx_config.pch $(ALL_INCS) \
		-Foobjs/src/http/modules/ngx_http_log_module.obj \
		src/http/modules/ngx_http_log_module.c


objs/src/http/ngx_http_request_body.obj:	$(CORE_DEPS) $(HTTP_DEPS) \
	src/http/ngx_http_request_body.c
	$(CC) -c $(CFLAGS) -Yungx_config.h -Fpobjs/ngx_config.pch $(ALL_INCS) \
		-Foobjs/src/http/ngx_http_request_body.obj \
		src/http/ngx_http_request_body.c


objs/src/http/ngx_http_variables.obj:	$(CORE_DEPS) $(HTTP_DEPS) \
	src/http/ngx_http_variables.c
	$(CC) -c $(CFLAGS) -Yungx_config.h -Fpobjs/ngx_config.pch $(ALL_INCS) \
		-Foobjs/src/http/ngx_http_variables.obj \
		src/http/ngx_http_variables.c


objs/src/http/ngx_http_script.obj:	$(CORE_DEPS) $(HTTP_DEPS) \
	src/http/ngx_http_script.c
	$(CC) -c $(CFLAGS) -Yungx_config.h -Fpobjs/ngx_config.pch $(ALL_INCS) \
		-Foobjs/src/http/ngx_http_script.obj \
		src/http/ngx_http_script.c


objs/src/http/ngx_http_upstream.obj:	$(CORE_DEPS) $(HTTP_DEPS) \
	src/http/ngx_http_upstream.c
	$(CC) -c $(CFLAGS) -Yungx_config.h -Fpobjs/ngx_config.pch $(ALL_INCS) \
		-Foobjs/src/http/ngx_http_upstream.obj \
		src/http/ngx_http_upstream.c


objs/src/http/ngx_http_upstream_round_robin.obj:	$(CORE_DEPS) $(HTTP_DEPS) \
	src/http/ngx_http_upstream_round_robin.c
	$(CC) -c $(CFLAGS) -Yungx_config.h -Fpobjs/ngx_config.pch $(ALL_INCS) \
		-Foobjs/src/http/ngx_http_upstream_round_robin.obj \
		src/http/ngx_http_upstream_round_robin.c


objs/src/http/ngx_http_file_cache.obj:	$(CORE_DEPS) $(HTTP_DEPS) \
	src/http/ngx_http_file_cache.c
	$(CC) -c $(CFLAGS) -Yungx_config.h -Fpobjs/ngx_config.pch $(ALL_INCS) \
		-Foobjs/src/http/ngx_http_file_cache.obj \
		src/http/ngx_http_file_cache.c


objs/src/http/ngx_http_write_filter_module.obj:	$(CORE_DEPS) $(HTTP_DEPS) \
	src/http/ngx_http_write_filter_module.c
	$(CC) -c $(CFLAGS) -Yungx_config.h -Fpobjs/ngx_config.pch $(ALL_INCS) \
		-Foobjs/src/http/ngx_http_write_filter_module.obj \
		src/http/ngx_http_write_filter_module.c


objs/src/http/ngx_http_header_filter_module.obj:	$(CORE_DEPS) $(HTTP_DEPS) \
	src/http/ngx_http_header_filter_module.c
	$(CC) -c $(CFLAGS) -Yungx_config.h -Fpobjs/ngx_config.pch $(ALL_INCS) \
		-Foobjs/src/http/ngx_http_header_filter_module.obj \
		src/http/ngx_http_header_filter_module.c


objs/src/http/modules/ngx_http_chunked_filter_module.obj:	$(CORE_DEPS) $(HTTP_DEPS) \
	src/http/modules/ngx_http_chunked_filter_module.c
	$(CC) -c $(CFLAGS) -Yungx_config.h -Fpobjs/ngx_config.pch $(ALL_INCS) \
		-Foobjs/src/http/modules/ngx_http_chunked_filter_module.obj \
		src/http/modules/ngx_http_chunked_filter_module.c


objs/src/http/modules/ngx_http_range_filter_module.obj:	$(CORE_DEPS) $(HTTP_DEPS) \
	src/http/modules/ngx_http_range_filter_module.c
	$(CC) -c $(CFLAGS) -Yungx_config.h -Fpobjs/ngx_config.pch $(ALL_INCS) \
		-Foobjs/src/http/modules/ngx_http_range_filter_module.obj \
		src/http/modules/ngx_http_range_filter_module.c


objs/src/http/modules/ngx_http_gzip_filter_module.obj:	$(CORE_DEPS) $(HTTP_DEPS) \
	src/http/modules/ngx_http_gzip_filter_module.c
	$(CC) -c $(CFLAGS) -Yungx_config.h -Fpobjs/ngx_config.pch $(ALL_INCS) \
		-Foobjs/src/http/modules/ngx_http_gzip_filter_module.obj \
		src/http/modules/ngx_http_gzip_filter_module.c


objs/src/http/ngx_http_postpone_filter_module.obj:	$(CORE_DEPS) $(HTTP_DEPS) \
	src/http/ngx_http_postpone_filter_module.c
	$(CC) -c $(CFLAGS) -Yungx_config.h -Fpobjs/ngx_config.pch $(ALL_INCS) \
		-Foobjs/src/http/ngx_http_postpone_filter_module.obj \
		src/http/ngx_http_postpone_filter_module.c


objs/src/http/modules/ngx_http_ssi_filter_module.obj:	$(CORE_DEPS) $(HTTP_DEPS) \
	src/http/modules/ngx_http_ssi_filter_module.c
	$(CC) -c $(CFLAGS) -Yungx_config.h -Fpobjs/ngx_config.pch $(ALL_INCS) \
		-Foobjs/src/http/modules/ngx_http_ssi_filter_module.obj \
		src/http/modules/ngx_http_ssi_filter_module.c


objs/src/http/modules/ngx_http_charset_filter_module.obj:	$(CORE_DEPS) $(HTTP_DEPS) \
	src/http/modules/ngx_http_charset_filter_module.c
	$(CC) -c $(CFLAGS) -Yungx_config.h -Fpobjs/ngx_config.pch $(ALL_INCS) \
		-Foobjs/src/http/modules/ngx_http_charset_filter_module.obj \
		src/http/modules/ngx_http_charset_filter_module.c


objs/src/http/modules/ngx_http_userid_filter_module.obj:	$(CORE_DEPS) $(HTTP_DEPS) \
	src/http/modules/ngx_http_userid_filter_module.c
	$(CC) -c $(CFLAGS) -Yungx_config.h -Fpobjs/ngx_config.pch $(ALL_INCS) \
		-Foobjs/src/http/modules/ngx_http_userid_filter_module.obj \
		src/http/modules/ngx_http_userid_filter_module.c


objs/src/http/modules/ngx_http_headers_filter_module.obj:	$(CORE_DEPS) $(HTTP_DEPS) \
	src/http/modules/ngx_http_headers_filter_module.c
	$(CC) -c $(CFLAGS) -Yungx_config.h -Fpobjs/ngx_config.pch $(ALL_INCS) \
		-Foobjs/src/http/modules/ngx_http_headers_filter_module.obj \
		src/http/modules/ngx_http_headers_filter_module.c


objs/src/http/ngx_http_copy_filter_module.obj:	$(CORE_DEPS) $(HTTP_DEPS) \
	src/http/ngx_http_copy_filter_module.c
	$(CC) -c $(CFLAGS) -Yungx_config.h -Fpobjs/ngx_config.pch $(ALL_INCS) \
		-Foobjs/src/http/ngx_http_copy_filter_module.obj \
		src/http/ngx_http_copy_filter_module.c


objs/src/http/modules/ngx_http_not_modified_filter_module.obj:	$(CORE_DEPS) $(HTTP_DEPS) \
	src/http/modules/ngx_http_not_modified_filter_module.c
	$(CC) -c $(CFLAGS) -Yungx_config.h -Fpobjs/ngx_config.pch $(ALL_INCS) \
		-Foobjs/src/http/modules/ngx_http_not_modified_filter_module.obj \
		src/http/modules/ngx_http_not_modified_filter_module.c


objs/src/http/modules/ngx_http_static_module.obj:	$(CORE_DEPS) $(HTTP_DEPS) \
	src/http/modules/ngx_http_static_module.c
	$(CC) -c $(CFLAGS) -Yungx_config.h -Fpobjs/ngx_config.pch $(ALL_INCS) \
		-Foobjs/src/http/modules/ngx_http_static_module.obj \
		src/http/modules/ngx_http_static_module.c


objs/src/http/modules/ngx_http_autoindex_module.obj:	$(CORE_DEPS) $(HTTP_DEPS) \
	src/http/modules/ngx_http_autoindex_module.c
	$(CC) -c $(CFLAGS) -Yungx_config.h -Fpobjs/ngx_config.pch $(ALL_INCS) \
		-Foobjs/src/http/modules/ngx_http_autoindex_module.obj \
		src/http/modules/ngx_http_autoindex_module.c


objs/src/http/modules/ngx_http_index_module.obj:	$(CORE_DEPS) $(HTTP_DEPS) \
	src/http/modules/ngx_http_index_module.c
	$(CC) -c $(CFLAGS) -Yungx_config.h -Fpobjs/ngx_config.pch $(ALL_INCS) \
		-Foobjs/src/http/modules/ngx_http_index_module.obj \
		src/http/modules/ngx_http_index_module.c


objs/src/http/modules/ngx_http_mirror_module.obj:	$(CORE_DEPS) $(HTTP_DEPS) \
	src/http/modules/ngx_http_mirror_module.c
	$(CC) -c $(CFLAGS) -Yungx_config.h -Fpobjs/ngx_config.pch $(ALL_INCS) \
		-Foobjs/src/http/modules/ngx_http_mirror_module.obj \
		src/http/modules/ngx_http_mirror_module.c


objs/src/http/modules/ngx_http_try_files_module.obj:	$(CORE_DEPS) $(HTTP_DEPS) \
	src/http/modules/ngx_http_try_files_module.c
	$(CC) -c $(CFLAGS) -Yungx_config.h -Fpobjs/ngx_config.pch $(ALL_INCS) \
		-Foobjs/src/http/modules/ngx_http_try_files_module.obj \
		src/http/modules/ngx_http_try_files_module.c


objs/src/http/modules/ngx_http_auth_basic_module.obj:	$(CORE_DEPS) $(HTTP_DEPS) \
	src/http/modules/ngx_http_auth_basic_module.c
	$(CC) -c $(CFLAGS) -Yungx_config.h -Fpobjs/ngx_config.pch $(ALL_INCS) \
		-Foobjs/src/http/modules/ngx_http_auth_basic_module.obj \
		src/http/modules/ngx_http_auth_basic_module.c


objs/src/http/modules/ngx_http_access_module.obj:	$(CORE_DEPS) $(HTTP_DEPS) \
	src/http/modules/ngx_http_access_module.c
	$(CC) -c $(CFLAGS) -Yungx_config.h -Fpobjs/ngx_config.pch $(ALL_INCS) \
		-Foobjs/src/http/modules/ngx_http_access_module.obj \
		src/http/modules/ngx_http_access_module.c


objs/src/http/modules/ngx_http_limit_conn_module.obj:	$(CORE_DEPS) $(HTTP_DEPS) \
	src/http/modules/ngx_http_limit_conn_module.c
	$(CC) -c $(CFLAGS) -Yungx_config.h -Fpobjs/ngx_config.pch $(ALL_INCS) \
		-Foobjs/src/http/modules/ngx_http_limit_conn_module.obj \
		src/http/modules/ngx_http_limit_conn_module.c


objs/src/http/modules/ngx_http_limit_req_module.obj:	$(CORE_DEPS) $(HTTP_DEPS) \
	src/http/modules/ngx_http_limit_req_module.c
	$(CC) -c $(CFLAGS) -Yungx_config.h -Fpobjs/ngx_config.pch $(ALL_INCS) \
		-Foobjs/src/http/modules/ngx_http_limit_req_module.obj \
		src/http/modules/ngx_http_limit_req_module.c


objs/src/http/modules/ngx_http_geo_module.obj:	$(CORE_DEPS) $(HTTP_DEPS) \
	src/http/modules/ngx_http_geo_module.c
	$(CC) -c $(CFLAGS) -Yungx_config.h -Fpobjs/ngx_config.pch $(ALL_INCS) \
		-Foobjs/src/http/modules/ngx_http_geo_module.obj \
		src/http/modules/ngx_http_geo_module.c


objs/src/http/modules/ngx_http_map_module.obj:	$(CORE_DEPS) $(HTTP_DEPS) \
	src/http/modules/ngx_http_map_module.c
	$(CC) -c $(CFLAGS) -Yungx_config.h -Fpobjs/ngx_config.pch $(ALL_INCS) \
		-Foobjs/src/http/modules/ngx_http_map_module.obj \
		src/http/modules/ngx_http_map_module.c


objs/src/http/modules/ngx_http_split_clients_module.obj:	$(CORE_DEPS) $(HTTP_DEPS) \
	src/http/modules/ngx_http_split_clients_module.c
	$(CC) -c $(CFLAGS) -Yungx_config.h -Fpobjs/ngx_config.pch $(ALL_INCS) \
		-Foobjs/src/http/modules/ngx_http_split_clients_module.obj \
		src/http/modules/ngx_http_split_clients_module.c


objs/src/http/modules/ngx_http_referer_module.obj:	$(CORE_DEPS) $(HTTP_DEPS) \
	src/http/modules/ngx_http_referer_module.c
	$(CC) -c $(CFLAGS) -Yungx_config.h -Fpobjs/ngx_config.pch $(ALL_INCS) \
		-Foobjs/src/http/modules/ngx_http_referer_module.obj \
		src/http/modules/ngx_http_referer_module.c


objs/src/http/modules/ngx_http_rewrite_module.obj:	$(CORE_DEPS) $(HTTP_DEPS) \
	src/http/modules/ngx_http_rewrite_module.c
	$(CC) -c $(CFLAGS) -Yungx_config.h -Fpobjs/ngx_config.pch $(ALL_INCS) \
		-Foobjs/src/http/modules/ngx_http_rewrite_module.obj \
		src/http/modules/ngx_http_rewrite_module.c


objs/src/http/modules/ngx_http_ssl_module.obj:	$(CORE_DEPS) $(HTTP_DEPS) \
	src/http/modules/ngx_http_ssl_module.c
	$(CC) -c $(CFLAGS) -Yungx_config.h -Fpobjs/ngx_config.pch $(ALL_INCS) \
		-Foobjs/src/http/modules/ngx_http_ssl_module.obj \
		src/http/modules/ngx_http_ssl_module.c


objs/src/http/modules/ngx_http_proxy_module.obj:	$(CORE_DEPS) $(HTTP_DEPS) \
	src/http/modules/ngx_http_proxy_module.c
	$(CC) -c $(CFLAGS) -Yungx_config.h -Fpobjs/ngx_config.pch $(ALL_INCS) \
		-Foobjs/src/http/modules/ngx_http_proxy_module.obj \
		src/http/modules/ngx_http_proxy_module.c


objs/src/http/modules/ngx_http_fastcgi_module.obj:	$(CORE_DEPS) $(HTTP_DEPS) \
	src/http/modules/ngx_http_fastcgi_module.c
	$(CC) -c $(CFLAGS) -Yungx_config.h -Fpobjs/ngx_config.pch $(ALL_INCS) \
		-Foobjs/src/http/modules/ngx_http_fastcgi_module.obj \
		src/http/modules/ngx_http_fastcgi_module.c


objs/src/http/modules/ngx_http_uwsgi_module.obj:	$(CORE_DEPS) $(HTTP_DEPS) \
	src/http/modules/ngx_http_uwsgi_module.c
	$(CC) -c $(CFLAGS) -Yungx_config.h -Fpobjs/ngx_config.pch $(ALL_INCS) \
		-Foobjs/src/http/modules/ngx_http_uwsgi_module.obj \
		src/http/modules/ngx_http_uwsgi_module.c


objs/src/http/modules/ngx_http_scgi_module.obj:	$(CORE_DEPS) $(HTTP_DEPS) \
	src/http/modules/ngx_http_scgi_module.c
	$(CC) -c $(CFLAGS) -Yungx_config.h -Fpobjs/ngx_config.pch $(ALL_INCS) \
		-Foobjs/src/http/modules/ngx_http_scgi_module.obj \
		src/http/modules/ngx_http_scgi_module.c


objs/src/http/modules/ngx_http_memcached_module.obj:	$(CORE_DEPS) $(HTTP_DEPS) \
	src/http/modules/ngx_http_memcached_module.c
	$(CC) -c $(CFLAGS) -Yungx_config.h -Fpobjs/ngx_config.pch $(ALL_INCS) \
		-Foobjs/src/http/modules/ngx_http_memcached_module.obj \
		src/http/modules/ngx_http_memcached_module.c


objs/src/http/modules/ngx_http_empty_gif_module.obj:	$(CORE_DEPS) $(HTTP_DEPS) \
	src/http/modules/ngx_http_empty_gif_module.c
	$(CC) -c $(CFLAGS) -Yungx_config.h -Fpobjs/ngx_config.pch $(ALL_INCS) \
		-Foobjs/src/http/modules/ngx_http_empty_gif_module.obj \
		src/http/modules/ngx_http_empty_gif_module.c


objs/src/http/modules/ngx_http_browser_module.obj:	$(CORE_DEPS) $(HTTP_DEPS) \
	src/http/modules/ngx_http_browser_module.c
	$(CC) -c $(CFLAGS) -Yungx_config.h -Fpobjs/ngx_config.pch $(ALL_INCS) \
		-Foobjs/src/http/modules/ngx_http_browser_module.obj \
		src/http/modules/ngx_http_browser_module.c


objs/src/http/modules/ngx_http_upstream_hash_module.obj:	$(CORE_DEPS) $(HTTP_DEPS) \
	src/http/modules/ngx_http_upstream_hash_module.c
	$(CC) -c $(CFLAGS) -Yungx_config.h -Fpobjs/ngx_config.pch $(ALL_INCS) \
		-Foobjs/src/http/modules/ngx_http_upstream_hash_module.obj \
		src/http/modules/ngx_http_upstream_hash_module.c


objs/src/http/modules/ngx_http_upstream_ip_hash_module.obj:	$(CORE_DEPS) $(HTTP_DEPS) \
	src/http/modules/ngx_http_upstream_ip_hash_module.c
	$(CC) -c $(CFLAGS) -Yungx_config.h -Fpobjs/ngx_config.pch $(ALL_INCS) \
		-Foobjs/src/http/modules/ngx_http_upstream_ip_hash_module.obj \
		src/http/modules/ngx_http_upstream_ip_hash_module.c


objs/src/http/modules/ngx_http_upstream_least_conn_module.obj:	$(CORE_DEPS) $(HTTP_DEPS) \
	src/http/modules/ngx_http_upstream_least_conn_module.c
	$(CC) -c $(CFLAGS) -Yungx_config.h -Fpobjs/ngx_config.pch $(ALL_INCS) \
		-Foobjs/src/http/modules/ngx_http_upstream_least_conn_module.obj \
		src/http/modules/ngx_http_upstream_least_conn_module.c


objs/src/http/modules/ngx_http_upstream_keepalive_module.obj:	$(CORE_DEPS) $(HTTP_DEPS) \
	src/http/modules/ngx_http_upstream_keepalive_module.c
	$(CC) -c $(CFLAGS) -Yungx_config.h -Fpobjs/ngx_config.pch $(ALL_INCS) \
		-Foobjs/src/http/modules/ngx_http_upstream_keepalive_module.obj \
		src/http/modules/ngx_http_upstream_keepalive_module.c


objs/src/http/modules/ngx_http_upstream_zone_module.obj:	$(CORE_DEPS) $(HTTP_DEPS) \
	src/http/modules/ngx_http_upstream_zone_module.c
	$(CC) -c $(CFLAGS) -Yungx_config.h -Fpobjs/ngx_config.pch $(ALL_INCS) \
		-Foobjs/src/http/modules/ngx_http_upstream_zone_module.obj \
		src/http/modules/ngx_http_upstream_zone_module.c


objs/addon/dash/edash_packager.obj:	$(ADDON_DEPS) \
	objs/lib/nginx-vod-module/vod/dash/edash_packager.c
	$(CC) -c $(CFLAGS) -Yungx_config.h -Fpobjs/ngx_config.pch $(ALL_INCS) \
		-Foobjs/addon/dash/edash_packager.obj \
		objs/lib/nginx-vod-module/vod/dash/edash_packager.c


objs/addon/hls/aes_cbc_encrypt.obj:	$(ADDON_DEPS) \
	objs/lib/nginx-vod-module/vod/hls/aes_cbc_encrypt.c
	$(CC) -c $(CFLAGS) -Yungx_config.h -Fpobjs/ngx_config.pch $(ALL_INCS) \
		-Foobjs/addon/hls/aes_cbc_encrypt.obj \
		objs/lib/nginx-vod-module/vod/hls/aes_cbc_encrypt.c


objs/addon/hls/eac3_encrypt_filter.obj:	$(ADDON_DEPS) \
	objs/lib/nginx-vod-module/vod/hls/eac3_encrypt_filter.c
	$(CC) -c $(CFLAGS) -Yungx_config.h -Fpobjs/ngx_config.pch $(ALL_INCS) \
		-Foobjs/addon/hls/eac3_encrypt_filter.obj \
		objs/lib/nginx-vod-module/vod/hls/eac3_encrypt_filter.c


objs/addon/hls/frame_encrypt_filter.obj:	$(ADDON_DEPS) \
	objs/lib/nginx-vod-module/vod/hls/frame_encrypt_filter.c
	$(CC) -c $(CFLAGS) -Yungx_config.h -Fpobjs/ngx_config.pch $(ALL_INCS) \
		-Foobjs/addon/hls/frame_encrypt_filter.obj \
		objs/lib/nginx-vod-module/vod/hls/frame_encrypt_filter.c


objs/addon/hls/sample_aes_avc_filter.obj:	$(ADDON_DEPS) \
	objs/lib/nginx-vod-module/vod/hls/sample_aes_avc_filter.c
	$(CC) -c $(CFLAGS) -Yungx_config.h -Fpobjs/ngx_config.pch $(ALL_INCS) \
		-Foobjs/addon/hls/sample_aes_avc_filter.obj \
		objs/lib/nginx-vod-module/vod/hls/sample_aes_avc_filter.c


objs/addon/mp4/mp4_aes_ctr.obj:	$(ADDON_DEPS) \
	objs/lib/nginx-vod-module/vod/mp4/mp4_aes_ctr.c
	$(CC) -c $(CFLAGS) -Yungx_config.h -Fpobjs/ngx_config.pch $(ALL_INCS) \
		-Foobjs/addon/mp4/mp4_aes_ctr.obj \
		objs/lib/nginx-vod-module/vod/mp4/mp4_aes_ctr.c


objs/addon/mp4/mp4_cbcs_encrypt.obj:	$(ADDON_DEPS) \
	objs/lib/nginx-vod-module/vod/mp4/mp4_cbcs_encrypt.c
	$(CC) -c $(CFLAGS) -Yungx_config.h -Fpobjs/ngx_config.pch $(ALL_INCS) \
		-Foobjs/addon/mp4/mp4_cbcs_encrypt.obj \
		objs/lib/nginx-vod-module/vod/mp4/mp4_cbcs_encrypt.c


objs/addon/mp4/mp4_cenc_decrypt.obj:	$(ADDON_DEPS) \
	objs/lib/nginx-vod-module/vod/mp4/mp4_cenc_decrypt.c
	$(CC) -c $(CFLAGS) -Yungx_config.h -Fpobjs/ngx_config.pch $(ALL_INCS) \
		-Foobjs/addon/mp4/mp4_cenc_decrypt.obj \
		objs/lib/nginx-vod-module/vod/mp4/mp4_cenc_decrypt.c


objs/addon/mp4/mp4_cenc_encrypt.obj:	$(ADDON_DEPS) \
	objs/lib/nginx-vod-module/vod/mp4/mp4_cenc_encrypt.c
	$(CC) -c $(CFLAGS) -Yungx_config.h -Fpobjs/ngx_config.pch $(ALL_INCS) \
		-Foobjs/addon/mp4/mp4_cenc_encrypt.obj \
		objs/lib/nginx-vod-module/vod/mp4/mp4_cenc_encrypt.c


objs/addon/mp4/mp4_cenc_passthrough.obj:	$(ADDON_DEPS) \
	objs/lib/nginx-vod-module/vod/mp4/mp4_cenc_passthrough.c
	$(CC) -c $(CFLAGS) -Yungx_config.h -Fpobjs/ngx_config.pch $(ALL_INCS) \
		-Foobjs/addon/mp4/mp4_cenc_passthrough.obj \
		objs/lib/nginx-vod-module/vod/mp4/mp4_cenc_passthrough.c


objs/addon/mss/mss_playready.obj:	$(ADDON_DEPS) \
	objs/lib/nginx-vod-module/vod/mss/mss_playready.c
	$(CC) -c $(CFLAGS) -Yungx_config.h -Fpobjs/ngx_config.pch $(ALL_INCS) \
		-Foobjs/addon/mss/mss_playready.obj \
		objs/lib/nginx-vod-module/vod/mss/mss_playready.c


objs/addon/nginx-vod-module/ngx_async_open_file_cache.obj:	$(ADDON_DEPS) \
	objs/lib/nginx-vod-module/ngx_async_open_file_cache.c
	$(CC) -c $(CFLAGS) -Yungx_config.h -Fpobjs/ngx_config.pch $(ALL_INCS) \
		-Foobjs/addon/nginx-vod-module/ngx_async_open_file_cache.obj \
		objs/lib/nginx-vod-module/ngx_async_open_file_cache.c


objs/addon/nginx-vod-module/ngx_buffer_cache.obj:	$(ADDON_DEPS) \
	objs/lib/nginx-vod-module/ngx_buffer_cache.c
	$(CC) -c $(CFLAGS) -Yungx_config.h -Fpobjs/ngx_config.pch $(ALL_INCS) \
		-Foobjs/addon/nginx-vod-module/ngx_buffer_cache.obj \
		objs/lib/nginx-vod-module/ngx_buffer_cache.c


objs/addon/nginx-vod-module/ngx_child_http_request.obj:	$(ADDON_DEPS) \
	objs/lib/nginx-vod-module/ngx_child_http_request.c
	$(CC) -c $(CFLAGS) -Yungx_config.h -Fpobjs/ngx_config.pch $(ALL_INCS) \
		-Foobjs/addon/nginx-vod-module/ngx_child_http_request.obj \
		objs/lib/nginx-vod-module/ngx_child_http_request.c


objs/addon/nginx-vod-module/ngx_file_reader.obj:	$(ADDON_DEPS) \
	objs/lib/nginx-vod-module/ngx_file_reader.c
	$(CC) -c $(CFLAGS) -Yungx_config.h -Fpobjs/ngx_config.pch $(ALL_INCS) \
		-Foobjs/addon/nginx-vod-module/ngx_file_reader.obj \
		objs/lib/nginx-vod-module/ngx_file_reader.c


objs/addon/nginx-vod-module/ngx_http_vod_conf.obj:	$(ADDON_DEPS) \
	objs/lib/nginx-vod-module/ngx_http_vod_conf.c
	$(CC) -c $(CFLAGS) -Yungx_config.h -Fpobjs/ngx_config.pch $(ALL_INCS) \
		-Foobjs/addon/nginx-vod-module/ngx_http_vod_conf.obj \
		objs/lib/nginx-vod-module/ngx_http_vod_conf.c


objs/addon/nginx-vod-module/ngx_http_vod_dash.obj:	$(ADDON_DEPS) \
	objs/lib/nginx-vod-module/ngx_http_vod_dash.c
	$(CC) -c $(CFLAGS) -Yungx_config.h -Fpobjs/ngx_config.pch $(ALL_INCS) \
		-Foobjs/addon/nginx-vod-module/ngx_http_vod_dash.obj \
		objs/lib/nginx-vod-module/ngx_http_vod_dash.c


objs/addon/nginx-vod-module/ngx_http_vod_hds.obj:	$(ADDON_DEPS) \
	objs/lib/nginx-vod-module/ngx_http_vod_hds.c
	$(CC) -c $(CFLAGS) -Yungx_config.h -Fpobjs/ngx_config.pch $(ALL_INCS) \
		-Foobjs/addon/nginx-vod-module/ngx_http_vod_hds.obj \
		objs/lib/nginx-vod-module/ngx_http_vod_hds.c


objs/addon/nginx-vod-module/ngx_http_vod_hls.obj:	$(ADDON_DEPS) \
	objs/lib/nginx-vod-module/ngx_http_vod_hls.c
	$(CC) -c $(CFLAGS) -Yungx_config.h -Fpobjs/ngx_config.pch $(ALL_INCS) \
		-Foobjs/addon/nginx-vod-module/ngx_http_vod_hls.obj \
		objs/lib/nginx-vod-module/ngx_http_vod_hls.c


objs/addon/nginx-vod-module/ngx_http_vod_module.obj:	$(ADDON_DEPS) \
	objs/lib/nginx-vod-module/ngx_http_vod_module.c
	$(CC) -c $(CFLAGS) -Yungx_config.h -Fpobjs/ngx_config.pch $(ALL_INCS) \
		-Foobjs/addon/nginx-vod-module/ngx_http_vod_module.obj \
		objs/lib/nginx-vod-module/ngx_http_vod_module.c


objs/addon/nginx-vod-module/ngx_http_vod_mss.obj:	$(ADDON_DEPS) \
	objs/lib/nginx-vod-module/ngx_http_vod_mss.c
	$(CC) -c $(CFLAGS) -Yungx_config.h -Fpobjs/ngx_config.pch $(ALL_INCS) \
		-Foobjs/addon/nginx-vod-module/ngx_http_vod_mss.obj \
		objs/lib/nginx-vod-module/ngx_http_vod_mss.c


objs/addon/nginx-vod-module/ngx_http_vod_request_parse.obj:	$(ADDON_DEPS) \
	objs/lib/nginx-vod-module/ngx_http_vod_request_parse.c
	$(CC) -c $(CFLAGS) -Yungx_config.h -Fpobjs/ngx_config.pch $(ALL_INCS) \
		-Foobjs/addon/nginx-vod-module/ngx_http_vod_request_parse.obj \
		objs/lib/nginx-vod-module/ngx_http_vod_request_parse.c


objs/addon/nginx-vod-module/ngx_http_vod_status.obj:	$(ADDON_DEPS) \
	objs/lib/nginx-vod-module/ngx_http_vod_status.c
	$(CC) -c $(CFLAGS) -Yungx_config.h -Fpobjs/ngx_config.pch $(ALL_INCS) \
		-Foobjs/addon/nginx-vod-module/ngx_http_vod_status.obj \
		objs/lib/nginx-vod-module/ngx_http_vod_status.c


objs/addon/nginx-vod-module/ngx_http_vod_submodule.obj:	$(ADDON_DEPS) \
	objs/lib/nginx-vod-module/ngx_http_vod_submodule.c
	$(CC) -c $(CFLAGS) -Yungx_config.h -Fpobjs/ngx_config.pch $(ALL_INCS) \
		-Foobjs/addon/nginx-vod-module/ngx_http_vod_submodule.obj \
		objs/lib/nginx-vod-module/ngx_http_vod_submodule.c


objs/addon/nginx-vod-module/ngx_http_vod_utils.obj:	$(ADDON_DEPS) \
	objs/lib/nginx-vod-module/ngx_http_vod_utils.c
	$(CC) -c $(CFLAGS) -Yungx_config.h -Fpobjs/ngx_config.pch $(ALL_INCS) \
		-Foobjs/addon/nginx-vod-module/ngx_http_vod_utils.obj \
		objs/lib/nginx-vod-module/ngx_http_vod_utils.c


objs/addon/nginx-vod-module/ngx_perf_counters.obj:	$(ADDON_DEPS) \
	objs/lib/nginx-vod-module/ngx_perf_counters.c
	$(CC) -c $(CFLAGS) -Yungx_config.h -Fpobjs/ngx_config.pch $(ALL_INCS) \
		-Foobjs/addon/nginx-vod-module/ngx_perf_counters.obj \
		objs/lib/nginx-vod-module/ngx_perf_counters.c


objs/addon/vod/avc_parser.obj:	$(ADDON_DEPS) \
	objs/lib/nginx-vod-module/vod/avc_parser.c
	$(CC) -c $(CFLAGS) -Yungx_config.h -Fpobjs/ngx_config.pch $(ALL_INCS) \
		-Foobjs/addon/vod/avc_parser.obj \
		objs/lib/nginx-vod-module/vod/avc_parser.c


objs/addon/vod/avc_hevc_parser.obj:	$(ADDON_DEPS) \
	objs/lib/nginx-vod-module/vod/avc_hevc_parser.c
	$(CC) -c $(CFLAGS) -Yungx_config.h -Fpobjs/ngx_config.pch $(ALL_INCS) \
		-Foobjs/addon/vod/avc_hevc_parser.obj \
		objs/lib/nginx-vod-module/vod/avc_hevc_parser.c


objs/addon/vod/buffer_pool.obj:	$(ADDON_DEPS) \
	objs/lib/nginx-vod-module/vod/buffer_pool.c
	$(CC) -c $(CFLAGS) -Yungx_config.h -Fpobjs/ngx_config.pch $(ALL_INCS) \
		-Foobjs/addon/vod/buffer_pool.obj \
		objs/lib/nginx-vod-module/vod/buffer_pool.c


objs/addon/vod/codec_config.obj:	$(ADDON_DEPS) \
	objs/lib/nginx-vod-module/vod/codec_config.c
	$(CC) -c $(CFLAGS) -Yungx_config.h -Fpobjs/ngx_config.pch $(ALL_INCS) \
		-Foobjs/addon/vod/codec_config.obj \
		objs/lib/nginx-vod-module/vod/codec_config.c


objs/addon/vod/common.obj:	$(ADDON_DEPS) \
	objs/lib/nginx-vod-module/vod/common.c
	$(CC) -c $(CFLAGS) -Yungx_config.h -Fpobjs/ngx_config.pch $(ALL_INCS) \
		-Foobjs/addon/vod/common.obj \
		objs/lib/nginx-vod-module/vod/common.c


objs/addon/dash/dash_packager.obj:	$(ADDON_DEPS) \
	objs/lib/nginx-vod-module/vod/dash/dash_packager.c
	$(CC) -c $(CFLAGS) -Yungx_config.h -Fpobjs/ngx_config.pch $(ALL_INCS) \
		-Foobjs/addon/dash/dash_packager.obj \
		objs/lib/nginx-vod-module/vod/dash/dash_packager.c


objs/addon/vod/dynamic_buffer.obj:	$(ADDON_DEPS) \
	objs/lib/nginx-vod-module/vod/dynamic_buffer.c
	$(CC) -c $(CFLAGS) -Yungx_config.h -Fpobjs/ngx_config.pch $(ALL_INCS) \
		-Foobjs/addon/vod/dynamic_buffer.obj \
		objs/lib/nginx-vod-module/vod/dynamic_buffer.c


objs/addon/filters/audio_filter.obj:	$(ADDON_DEPS) \
	objs/lib/nginx-vod-module/vod/filters/audio_filter.c
	$(CC) -c $(CFLAGS) -Yungx_config.h -Fpobjs/ngx_config.pch $(ALL_INCS) \
		-Foobjs/addon/filters/audio_filter.obj \
		objs/lib/nginx-vod-module/vod/filters/audio_filter.c


objs/addon/filters/concat_clip.obj:	$(ADDON_DEPS) \
	objs/lib/nginx-vod-module/vod/filters/concat_clip.c
	$(CC) -c $(CFLAGS) -Yungx_config.h -Fpobjs/ngx_config.pch $(ALL_INCS) \
		-Foobjs/addon/filters/concat_clip.obj \
		objs/lib/nginx-vod-module/vod/filters/concat_clip.c


objs/addon/filters/dynamic_clip.obj:	$(ADDON_DEPS) \
	objs/lib/nginx-vod-module/vod/filters/dynamic_clip.c
	$(CC) -c $(CFLAGS) -Yungx_config.h -Fpobjs/ngx_config.pch $(ALL_INCS) \
		-Foobjs/addon/filters/dynamic_clip.obj \
		objs/lib/nginx-vod-module/vod/filters/dynamic_clip.c


objs/addon/filters/filter.obj:	$(ADDON_DEPS) \
	objs/lib/nginx-vod-module/vod/filters/filter.c
	$(CC) -c $(CFLAGS) -Yungx_config.h -Fpobjs/ngx_config.pch $(ALL_INCS) \
		-Foobjs/addon/filters/filter.obj \
		objs/lib/nginx-vod-module/vod/filters/filter.c


objs/addon/filters/gain_filter.obj:	$(ADDON_DEPS) \
	objs/lib/nginx-vod-module/vod/filters/gain_filter.c
	$(CC) -c $(CFLAGS) -Yungx_config.h -Fpobjs/ngx_config.pch $(ALL_INCS) \
		-Foobjs/addon/filters/gain_filter.obj \
		objs/lib/nginx-vod-module/vod/filters/gain_filter.c


objs/addon/filters/mix_filter.obj:	$(ADDON_DEPS) \
	objs/lib/nginx-vod-module/vod/filters/mix_filter.c
	$(CC) -c $(CFLAGS) -Yungx_config.h -Fpobjs/ngx_config.pch $(ALL_INCS) \
		-Foobjs/addon/filters/mix_filter.obj \
		objs/lib/nginx-vod-module/vod/filters/mix_filter.c


objs/addon/filters/rate_filter.obj:	$(ADDON_DEPS) \
	objs/lib/nginx-vod-module/vod/filters/rate_filter.c
	$(CC) -c $(CFLAGS) -Yungx_config.h -Fpobjs/ngx_config.pch $(ALL_INCS) \
		-Foobjs/addon/filters/rate_filter.obj \
		objs/lib/nginx-vod-module/vod/filters/rate_filter.c


objs/addon/hds/hds_amf0_encoder.obj:	$(ADDON_DEPS) \
	objs/lib/nginx-vod-module/vod/hds/hds_amf0_encoder.c
	$(CC) -c $(CFLAGS) -Yungx_config.h -Fpobjs/ngx_config.pch $(ALL_INCS) \
		-Foobjs/addon/hds/hds_amf0_encoder.obj \
		objs/lib/nginx-vod-module/vod/hds/hds_amf0_encoder.c


objs/addon/hds/hds_fragment.obj:	$(ADDON_DEPS) \
	objs/lib/nginx-vod-module/vod/hds/hds_fragment.c
	$(CC) -c $(CFLAGS) -Yungx_config.h -Fpobjs/ngx_config.pch $(ALL_INCS) \
		-Foobjs/addon/hds/hds_fragment.obj \
		objs/lib/nginx-vod-module/vod/hds/hds_fragment.c


objs/addon/hds/hds_manifest.obj:	$(ADDON_DEPS) \
	objs/lib/nginx-vod-module/vod/hds/hds_manifest.c
	$(CC) -c $(CFLAGS) -Yungx_config.h -Fpobjs/ngx_config.pch $(ALL_INCS) \
		-Foobjs/addon/hds/hds_manifest.obj \
		objs/lib/nginx-vod-module/vod/hds/hds_manifest.c


objs/addon/vod/hevc_parser.obj:	$(ADDON_DEPS) \
	objs/lib/nginx-vod-module/vod/hevc_parser.c
	$(CC) -c $(CFLAGS) -Yungx_config.h -Fpobjs/ngx_config.pch $(ALL_INCS) \
		-Foobjs/addon/vod/hevc_parser.obj \
		objs/lib/nginx-vod-module/vod/hevc_parser.c


objs/addon/hls/adts_encoder_filter.obj:	$(ADDON_DEPS) \
	objs/lib/nginx-vod-module/vod/hls/adts_encoder_filter.c
	$(CC) -c $(CFLAGS) -Yungx_config.h -Fpobjs/ngx_config.pch $(ALL_INCS) \
		-Foobjs/addon/hls/adts_encoder_filter.obj \
		objs/lib/nginx-vod-module/vod/hls/adts_encoder_filter.c


objs/addon/hls/buffer_filter.obj:	$(ADDON_DEPS) \
	objs/lib/nginx-vod-module/vod/hls/buffer_filter.c
	$(CC) -c $(CFLAGS) -Yungx_config.h -Fpobjs/ngx_config.pch $(ALL_INCS) \
		-Foobjs/addon/hls/buffer_filter.obj \
		objs/lib/nginx-vod-module/vod/hls/buffer_filter.c


objs/addon/hls/frame_joiner_filter.obj:	$(ADDON_DEPS) \
	objs/lib/nginx-vod-module/vod/hls/frame_joiner_filter.c
	$(CC) -c $(CFLAGS) -Yungx_config.h -Fpobjs/ngx_config.pch $(ALL_INCS) \
		-Foobjs/addon/hls/frame_joiner_filter.obj \
		objs/lib/nginx-vod-module/vod/hls/frame_joiner_filter.c


objs/addon/hls/hls_muxer.obj:	$(ADDON_DEPS) \
	objs/lib/nginx-vod-module/vod/hls/hls_muxer.c
	$(CC) -c $(CFLAGS) -Yungx_config.h -Fpobjs/ngx_config.pch $(ALL_INCS) \
		-Foobjs/addon/hls/hls_muxer.obj \
		objs/lib/nginx-vod-module/vod/hls/hls_muxer.c


objs/addon/hls/id3_encoder_filter.obj:	$(ADDON_DEPS) \
	objs/lib/nginx-vod-module/vod/hls/id3_encoder_filter.c
	$(CC) -c $(CFLAGS) -Yungx_config.h -Fpobjs/ngx_config.pch $(ALL_INCS) \
		-Foobjs/addon/hls/id3_encoder_filter.obj \
		objs/lib/nginx-vod-module/vod/hls/id3_encoder_filter.c


objs/addon/hls/m3u8_builder.obj:	$(ADDON_DEPS) \
	objs/lib/nginx-vod-module/vod/hls/m3u8_builder.c
	$(CC) -c $(CFLAGS) -Yungx_config.h -Fpobjs/ngx_config.pch $(ALL_INCS) \
		-Foobjs/addon/hls/m3u8_builder.obj \
		objs/lib/nginx-vod-module/vod/hls/m3u8_builder.c


objs/addon/hls/mp4_to_annexb_filter.obj:	$(ADDON_DEPS) \
	objs/lib/nginx-vod-module/vod/hls/mp4_to_annexb_filter.c
	$(CC) -c $(CFLAGS) -Yungx_config.h -Fpobjs/ngx_config.pch $(ALL_INCS) \
		-Foobjs/addon/hls/mp4_to_annexb_filter.obj \
		objs/lib/nginx-vod-module/vod/hls/mp4_to_annexb_filter.c


objs/addon/hls/mpegts_encoder_filter.obj:	$(ADDON_DEPS) \
	objs/lib/nginx-vod-module/vod/hls/mpegts_encoder_filter.c
	$(CC) -c $(CFLAGS) -Yungx_config.h -Fpobjs/ngx_config.pch $(ALL_INCS) \
		-Foobjs/addon/hls/mpegts_encoder_filter.obj \
		objs/lib/nginx-vod-module/vod/hls/mpegts_encoder_filter.c


objs/addon/input/silence_generator.obj:	$(ADDON_DEPS) \
	objs/lib/nginx-vod-module/vod/input/silence_generator.c
	$(CC) -c $(CFLAGS) -Yungx_config.h -Fpobjs/ngx_config.pch $(ALL_INCS) \
		-Foobjs/addon/input/silence_generator.obj \
		objs/lib/nginx-vod-module/vod/input/silence_generator.c


objs/addon/input/frames_source_cache.obj:	$(ADDON_DEPS) \
	objs/lib/nginx-vod-module/vod/input/frames_source_cache.c
	$(CC) -c $(CFLAGS) -Yungx_config.h -Fpobjs/ngx_config.pch $(ALL_INCS) \
		-Foobjs/addon/input/frames_source_cache.obj \
		objs/lib/nginx-vod-module/vod/input/frames_source_cache.c


objs/addon/input/frames_source_memory.obj:	$(ADDON_DEPS) \
	objs/lib/nginx-vod-module/vod/input/frames_source_memory.c
	$(CC) -c $(CFLAGS) -Yungx_config.h -Fpobjs/ngx_config.pch $(ALL_INCS) \
		-Foobjs/addon/input/frames_source_memory.obj \
		objs/lib/nginx-vod-module/vod/input/frames_source_memory.c


objs/addon/input/read_cache.obj:	$(ADDON_DEPS) \
	objs/lib/nginx-vod-module/vod/input/read_cache.c
	$(CC) -c $(CFLAGS) -Yungx_config.h -Fpobjs/ngx_config.pch $(ALL_INCS) \
		-Foobjs/addon/input/read_cache.obj \
		objs/lib/nginx-vod-module/vod/input/read_cache.c


objs/addon/vod/json_parser.obj:	$(ADDON_DEPS) \
	objs/lib/nginx-vod-module/vod/json_parser.c
	$(CC) -c $(CFLAGS) -Yungx_config.h -Fpobjs/ngx_config.pch $(ALL_INCS) \
		-Foobjs/addon/vod/json_parser.obj \
		objs/lib/nginx-vod-module/vod/json_parser.c


objs/addon/vod/language_code.obj:	$(ADDON_DEPS) \
	objs/lib/nginx-vod-module/vod/language_code.c
	$(CC) -c $(CFLAGS) -Yungx_config.h -Fpobjs/ngx_config.pch $(ALL_INCS) \
		-Foobjs/addon/vod/language_code.obj \
		objs/lib/nginx-vod-module/vod/language_code.c


objs/addon/vod/manifest_utils.obj:	$(ADDON_DEPS) \
	objs/lib/nginx-vod-module/vod/manifest_utils.c
	$(CC) -c $(CFLAGS) -Yungx_config.h -Fpobjs/ngx_config.pch $(ALL_INCS) \
		-Foobjs/addon/vod/manifest_utils.obj \
		objs/lib/nginx-vod-module/vod/manifest_utils.c


objs/addon/vod/media_format.obj:	$(ADDON_DEPS) \
	objs/lib/nginx-vod-module/vod/media_format.c
	$(CC) -c $(CFLAGS) -Yungx_config.h -Fpobjs/ngx_config.pch $(ALL_INCS) \
		-Foobjs/addon/vod/media_format.obj \
		objs/lib/nginx-vod-module/vod/media_format.c


objs/addon/vod/media_set_parser.obj:	$(ADDON_DEPS) \
	objs/lib/nginx-vod-module/vod/media_set_parser.c
	$(CC) -c $(CFLAGS) -Yungx_config.h -Fpobjs/ngx_config.pch $(ALL_INCS) \
		-Foobjs/addon/vod/media_set_parser.obj \
		objs/lib/nginx-vod-module/vod/media_set_parser.c


objs/addon/mkv/ebml.obj:	$(ADDON_DEPS) \
	objs/lib/nginx-vod-module/vod/mkv/ebml.c
	$(CC) -c $(CFLAGS) -Yungx_config.h -Fpobjs/ngx_config.pch $(ALL_INCS) \
		-Foobjs/addon/mkv/ebml.obj \
		objs/lib/nginx-vod-module/vod/mkv/ebml.c


objs/addon/mkv/mkv_builder.obj:	$(ADDON_DEPS) \
	objs/lib/nginx-vod-module/vod/mkv/mkv_builder.c
	$(CC) -c $(CFLAGS) -Yungx_config.h -Fpobjs/ngx_config.pch $(ALL_INCS) \
		-Foobjs/addon/mkv/mkv_builder.obj \
		objs/lib/nginx-vod-module/vod/mkv/mkv_builder.c


objs/addon/mkv/mkv_defs.obj:	$(ADDON_DEPS) \
	objs/lib/nginx-vod-module/vod/mkv/mkv_defs.c
	$(CC) -c $(CFLAGS) -Yungx_config.h -Fpobjs/ngx_config.pch $(ALL_INCS) \
		-Foobjs/addon/mkv/mkv_defs.obj \
		objs/lib/nginx-vod-module/vod/mkv/mkv_defs.c


objs/addon/mkv/mkv_format.obj:	$(ADDON_DEPS) \
	objs/lib/nginx-vod-module/vod/mkv/mkv_format.c
	$(CC) -c $(CFLAGS) -Yungx_config.h -Fpobjs/ngx_config.pch $(ALL_INCS) \
		-Foobjs/addon/mkv/mkv_format.obj \
		objs/lib/nginx-vod-module/vod/mkv/mkv_format.c


objs/addon/mp4/mp4_format.obj:	$(ADDON_DEPS) \
	objs/lib/nginx-vod-module/vod/mp4/mp4_format.c
	$(CC) -c $(CFLAGS) -Yungx_config.h -Fpobjs/ngx_config.pch $(ALL_INCS) \
		-Foobjs/addon/mp4/mp4_format.obj \
		objs/lib/nginx-vod-module/vod/mp4/mp4_format.c


objs/addon/mp4/mp4_fragment.obj:	$(ADDON_DEPS) \
	objs/lib/nginx-vod-module/vod/mp4/mp4_fragment.c
	$(CC) -c $(CFLAGS) -Yungx_config.h -Fpobjs/ngx_config.pch $(ALL_INCS) \
		-Foobjs/addon/mp4/mp4_fragment.obj \
		objs/lib/nginx-vod-module/vod/mp4/mp4_fragment.c


objs/addon/mp4/mp4_init_segment.obj:	$(ADDON_DEPS) \
	objs/lib/nginx-vod-module/vod/mp4/mp4_init_segment.c
	$(CC) -c $(CFLAGS) -Yungx_config.h -Fpobjs/ngx_config.pch $(ALL_INCS) \
		-Foobjs/addon/mp4/mp4_init_segment.obj \
		objs/lib/nginx-vod-module/vod/mp4/mp4_init_segment.c


objs/addon/mp4/mp4_muxer.obj:	$(ADDON_DEPS) \
	objs/lib/nginx-vod-module/vod/mp4/mp4_muxer.c
	$(CC) -c $(CFLAGS) -Yungx_config.h -Fpobjs/ngx_config.pch $(ALL_INCS) \
		-Foobjs/addon/mp4/mp4_muxer.obj \
		objs/lib/nginx-vod-module/vod/mp4/mp4_muxer.c


objs/addon/mp4/mp4_parser.obj:	$(ADDON_DEPS) \
	objs/lib/nginx-vod-module/vod/mp4/mp4_parser.c
	$(CC) -c $(CFLAGS) -Yungx_config.h -Fpobjs/ngx_config.pch $(ALL_INCS) \
		-Foobjs/addon/mp4/mp4_parser.obj \
		objs/lib/nginx-vod-module/vod/mp4/mp4_parser.c


objs/addon/mp4/mp4_clipper.obj:	$(ADDON_DEPS) \
	objs/lib/nginx-vod-module/vod/mp4/mp4_clipper.c
	$(CC) -c $(CFLAGS) -Yungx_config.h -Fpobjs/ngx_config.pch $(ALL_INCS) \
		-Foobjs/addon/mp4/mp4_clipper.obj \
		objs/lib/nginx-vod-module/vod/mp4/mp4_clipper.c


objs/addon/mp4/mp4_parser_base.obj:	$(ADDON_DEPS) \
	objs/lib/nginx-vod-module/vod/mp4/mp4_parser_base.c
	$(CC) -c $(CFLAGS) -Yungx_config.h -Fpobjs/ngx_config.pch $(ALL_INCS) \
		-Foobjs/addon/mp4/mp4_parser_base.obj \
		objs/lib/nginx-vod-module/vod/mp4/mp4_parser_base.c


objs/addon/mss/mss_packager.obj:	$(ADDON_DEPS) \
	objs/lib/nginx-vod-module/vod/mss/mss_packager.c
	$(CC) -c $(CFLAGS) -Yungx_config.h -Fpobjs/ngx_config.pch $(ALL_INCS) \
		-Foobjs/addon/mss/mss_packager.obj \
		objs/lib/nginx-vod-module/vod/mss/mss_packager.c


objs/addon/subtitle/cap_format.obj:	$(ADDON_DEPS) \
	objs/lib/nginx-vod-module/vod/subtitle/cap_format.c
	$(CC) -c $(CFLAGS) -Yungx_config.h -Fpobjs/ngx_config.pch $(ALL_INCS) \
		-Foobjs/addon/subtitle/cap_format.obj \
		objs/lib/nginx-vod-module/vod/subtitle/cap_format.c


objs/addon/subtitle/subtitle_format.obj:	$(ADDON_DEPS) \
	objs/lib/nginx-vod-module/vod/subtitle/subtitle_format.c
	$(CC) -c $(CFLAGS) -Yungx_config.h -Fpobjs/ngx_config.pch $(ALL_INCS) \
		-Foobjs/addon/subtitle/subtitle_format.obj \
		objs/lib/nginx-vod-module/vod/subtitle/subtitle_format.c


objs/addon/subtitle/ttml_builder.obj:	$(ADDON_DEPS) \
	objs/lib/nginx-vod-module/vod/subtitle/ttml_builder.c
	$(CC) -c $(CFLAGS) -Yungx_config.h -Fpobjs/ngx_config.pch $(ALL_INCS) \
		-Foobjs/addon/subtitle/ttml_builder.obj \
		objs/lib/nginx-vod-module/vod/subtitle/ttml_builder.c


objs/addon/subtitle/webvtt_builder.obj:	$(ADDON_DEPS) \
	objs/lib/nginx-vod-module/vod/subtitle/webvtt_builder.c
	$(CC) -c $(CFLAGS) -Yungx_config.h -Fpobjs/ngx_config.pch $(ALL_INCS) \
		-Foobjs/addon/subtitle/webvtt_builder.obj \
		objs/lib/nginx-vod-module/vod/subtitle/webvtt_builder.c


objs/addon/subtitle/webvtt_format.obj:	$(ADDON_DEPS) \
	objs/lib/nginx-vod-module/vod/subtitle/webvtt_format.c
	$(CC) -c $(CFLAGS) -Yungx_config.h -Fpobjs/ngx_config.pch $(ALL_INCS) \
		-Foobjs/addon/subtitle/webvtt_format.obj \
		objs/lib/nginx-vod-module/vod/subtitle/webvtt_format.c


objs/addon/vod/parse_utils.obj:	$(ADDON_DEPS) \
	objs/lib/nginx-vod-module/vod/parse_utils.c
	$(CC) -c $(CFLAGS) -Yungx_config.h -Fpobjs/ngx_config.pch $(ALL_INCS) \
		-Foobjs/addon/vod/parse_utils.obj \
		objs/lib/nginx-vod-module/vod/parse_utils.c


objs/addon/vod/segmenter.obj:	$(ADDON_DEPS) \
	objs/lib/nginx-vod-module/vod/segmenter.c
	$(CC) -c $(CFLAGS) -Yungx_config.h -Fpobjs/ngx_config.pch $(ALL_INCS) \
		-Foobjs/addon/vod/segmenter.obj \
		objs/lib/nginx-vod-module/vod/segmenter.c


objs/addon/vod/udrm.obj:	$(ADDON_DEPS) \
	objs/lib/nginx-vod-module/vod/udrm.c
	$(CC) -c $(CFLAGS) -Yungx_config.h -Fpobjs/ngx_config.pch $(ALL_INCS) \
		-Foobjs/addon/vod/udrm.obj \
		objs/lib/nginx-vod-module/vod/udrm.c


objs/addon/vod/write_buffer.obj:	$(ADDON_DEPS) \
	objs/lib/nginx-vod-module/vod/write_buffer.c
	$(CC) -c $(CFLAGS) -Yungx_config.h -Fpobjs/ngx_config.pch $(ALL_INCS) \
		-Foobjs/addon/vod/write_buffer.obj \
		objs/lib/nginx-vod-module/vod/write_buffer.c


objs/addon/vod/write_buffer_queue.obj:	$(ADDON_DEPS) \
	objs/lib/nginx-vod-module/vod/write_buffer_queue.c
	$(CC) -c $(CFLAGS) -Yungx_config.h -Fpobjs/ngx_config.pch $(ALL_INCS) \
		-Foobjs/addon/vod/write_buffer_queue.obj \
		objs/lib/nginx-vod-module/vod/write_buffer_queue.c


objs/nginx.res:	 src/os/win32/nginx.ico
	rc -foobjs/nginx.res $(CORE_INCS) src/os/win32/nginx.rc


objs/ngx_config.pch:	src/core/ngx_config.h src/os/win32/ngx_win32_config.h objs/ngx_auto_config.h
	$(CC) $(CFLAGS) -Ycngx_config.h -Fpobjs/ngx_config.pch -c $(ALL_INCS) -Foobjs/ngx_pch.obj objs/ngx_pch.c


objs/lib/pcre-8.40/pcre.lib:	objs/lib/pcre-8.40/pcre.h objs/Makefile
	$(MAKE) -f auto/lib/pcre/makefile.msvc PCRE="objs/lib/pcre-8.40" CPU_OPT="" LIBC=-MT

objs/lib/pcre-8.40/pcre.h:
	$(MAKE) -f auto/lib/pcre/makefile.msvc PCRE="objs/lib/pcre-8.40" pcre.h


objs/lib/openssl/openssl/include/openssl/ssl.h:	objs/Makefile
	$(MAKE) -f auto/lib/openssl/makefile.msvc					OPENSSL="objs/lib/openssl" OPENSSL_OPT="no-asm"


objs/lib/zlib/zlib.lib:	objs/Makefile
	$(MAKE) -f auto/lib/zlib/makefile.msvc CPU_OPT="" LIBC=-MT ZLIB="objs/lib/zlib"


manpage:	objs/nginx.8

objs/nginx.8:	docs/man/nginx.8 objs/ngx_auto_config.h
	sed -e "s|%%PREFIX%%||" \
		-e "s|%%PID_PATH%%|/logs/nginx.pid|" \
		-e "s|%%CONF_PATH%%|/conf/nginx.conf|" \
		-e "s|%%ERROR_LOG_PATH%%|/logs/error.log|" \
		< docs/man/nginx.8 > $@

install:	build 
	test -d '$(DESTDIR)' || mkdir -p '$(DESTDIR)'

	test -d '$(DESTDIR)/' \
		|| mkdir -p '$(DESTDIR)/'
	test ! -f '$(DESTDIR)/nginx.exe' \
		|| mv '$(DESTDIR)/nginx.exe' \
			'$(DESTDIR)/nginx.exe.old'
	cp objs/nginx '$(DESTDIR)/nginx.exe'

	test -d '$(DESTDIR)/conf' \
		|| mkdir -p '$(DESTDIR)/conf'

	cp conf/koi-win '$(DESTDIR)/conf'
	cp conf/koi-utf '$(DESTDIR)/conf'
	cp conf/win-utf '$(DESTDIR)/conf'

	test -f '$(DESTDIR)/conf/mime.types' \
		|| cp conf/mime.types '$(DESTDIR)/conf'
	cp conf/mime.types '$(DESTDIR)/conf/mime.types.default'

	test -f '$(DESTDIR)/conf/fastcgi_params' \
		|| cp conf/fastcgi_params '$(DESTDIR)/conf'
	cp conf/fastcgi_params \
		'$(DESTDIR)/conf/fastcgi_params.default'

	test -f '$(DESTDIR)/conf/fastcgi.conf' \
		|| cp conf/fastcgi.conf '$(DESTDIR)/conf'
	cp conf/fastcgi.conf '$(DESTDIR)/conf/fastcgi.conf.default'

	test -f '$(DESTDIR)/conf/uwsgi_params' \
		|| cp conf/uwsgi_params '$(DESTDIR)/conf'
	cp conf/uwsgi_params \
		'$(DESTDIR)/conf/uwsgi_params.default'

	test -f '$(DESTDIR)/conf/scgi_params' \
		|| cp conf/scgi_params '$(DESTDIR)/conf'
	cp conf/scgi_params \
		'$(DESTDIR)/conf/scgi_params.default'

	test -f '$(DESTDIR)/conf/nginx.conf' \
		|| cp conf/nginx.conf '$(DESTDIR)/conf/nginx.conf'
	cp conf/nginx.conf '$(DESTDIR)/conf/nginx.conf.default'

	test -d '$(DESTDIR)/logs' \
		|| mkdir -p '$(DESTDIR)/logs'

	test -d '$(DESTDIR)/logs' \
		|| mkdir -p '$(DESTDIR)/logs'

	test -d '$(DESTDIR)/html' \
		|| cp -R docs/html '$(DESTDIR)'

	test -d '$(DESTDIR)/logs' \
		|| mkdir -p '$(DESTDIR)/logs'
