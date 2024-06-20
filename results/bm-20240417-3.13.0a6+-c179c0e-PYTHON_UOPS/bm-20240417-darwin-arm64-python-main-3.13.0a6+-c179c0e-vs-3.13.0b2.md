# Results vs. 3.13.0b2

- fork: python
- ref: main
- machine: darwin-arm64
- commit hash: c179c0e
- commit date: 2024-04-17
- overall geometric mean: 1.15x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.09x slower
- Memory change: 0.97x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240605-darwin-arm64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240417-darwin-arm64-python-main-3.13.0a6+-c179c0e |
|----------------|:----------------------------------------------------------:|:------------------------------------------------------:|
| 2to3           | 161 ms                                                     | 179 ms: 1.11x slower                                   |
| chameleon      | 4.27 ms                                                    | 4.81 ms: 1.13x slower                                  |
| docutils       | 1.44 sec                                                   | 1.61 sec: 1.12x slower                                 |
| html5lib       | 31.2 ms                                                    | 33.0 ms: 1.06x slower                                  |
| tornado_http   | 66.7 ms                                                    | 84.3 ms: 1.26x slower                                  |
| Geometric mean | (ref)                                                      | 1.13x slower                                           |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240605-darwin-arm64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240417-darwin-arm64-python-main-3.13.0a6+-c179c0e |
|----------------------------------|:----------------------------------------------------------:|:------------------------------------------------------:|
| async_tree_eager_cpu_io_mixed_tg | 331 ms                                                     | 338 ms: 1.02x slower                                   |
| async_tree_none                  | 209 ms                                                     | 216 ms: 1.03x slower                                   |
| async_tree_eager_cpu_io_mixed    | 358 ms                                                     | 370 ms: 1.03x slower                                   |
| async_tree_io                    | 563 ms                                                     | 586 ms: 1.04x slower                                   |
| async_tree_eager_io              | 766 ms                                                     | 798 ms: 1.04x slower                                   |
| async_tree_eager_memoization     | 152 ms                                                     | 160 ms: 1.05x slower                                   |
| async_tree_none_tg               | 198 ms                                                     | 208 ms: 1.05x slower                                   |
| async_tree_cpu_io_mixed_tg       | 451 ms                                                     | 475 ms: 1.05x slower                                   |
| async_tree_eager_memoization_tg  | 126 ms                                                     | 134 ms: 1.07x slower                                   |
| async_tree_memoization           | 260 ms                                                     | 284 ms: 1.10x slower                                   |
| async_tree_memoization_tg        | 240 ms                                                     | 271 ms: 1.13x slower                                   |
| async_tree_eager_tg              | 41.4 ms                                                    | 47.0 ms: 1.14x slower                                  |
| async_tree_eager                 | 60.3 ms                                                    | 71.4 ms: 1.18x slower                                  |
| Geometric mean                   | (ref)                                                      | 1.06x slower                                           |

Benchmark hidden because not significant (3): async_tree_eager_io_tg, async_tree_cpu_io_mixed, async_tree_io_tg

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240605-darwin-arm64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240417-darwin-arm64-python-main-3.13.0a6+-c179c0e |
|----------------|:----------------------------------------------------------:|:------------------------------------------------------:|
| pidigits       | 282 ms                                                     | 284 ms: 1.01x slower                                   |
| float          | 48.6 ms                                                    | 75.1 ms: 1.55x slower                                  |
| nbody          | 59.6 ms                                                    | 97.8 ms: 1.64x slower                                  |
| Geometric mean | (ref)                                                      | 1.37x slower                                           |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240605-darwin-arm64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240417-darwin-arm64-python-main-3.13.0a6+-c179c0e |
|----------------|:----------------------------------------------------------:|:------------------------------------------------------:|
| regex_v8       | 17.3 ms                                                    | 17.8 ms: 1.03x slower                                  |
| regex_compile  | 68.5 ms                                                    | 102 ms: 1.49x slower                                   |
| Geometric mean | (ref)                                                      | 1.11x slower                                           |

Benchmark hidden because not significant (2): regex_dna, regex_effbot

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240605-darwin-arm64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240417-darwin-arm64-python-main-3.13.0a6+-c179c0e |
|----------------------|:----------------------------------------------------------:|:------------------------------------------------------:|
| pickle_dict          | 18.3 us                                                    | 18.2 us: 1.00x faster                                  |
| pickle               | 7.48 us                                                    | 7.51 us: 1.00x slower                                  |
| json_dumps           | 6.23 ms                                                    | 6.27 ms: 1.01x slower                                  |
| json_loads           | 16.8 us                                                    | 16.9 us: 1.01x slower                                  |
| unpickle_list        | 2.88 us                                                    | 2.92 us: 1.01x slower                                  |
| pickle_list          | 2.96 us                                                    | 3.01 us: 1.02x slower                                  |
| unpickle             | 9.12 us                                                    | 9.29 us: 1.02x slower                                  |
| pickle_pure_python   | 179 us                                                     | 186 us: 1.04x slower                                   |
| xml_etree_process    | 37.1 ms                                                    | 40.7 ms: 1.10x slower                                  |
| xml_etree_generate   | 52.7 ms                                                    | 59.4 ms: 1.13x slower                                  |
| xml_etree_iterparse  | 71.5 ms                                                    | 80.9 ms: 1.13x slower                                  |
| tomli_loads          | 1.47 sec                                                   | 1.83 sec: 1.25x slower                                 |
| unpickle_pure_python | 141 us                                                     | 202 us: 1.43x slower                                   |
| Geometric mean       | (ref)                                                      | 1.08x slower                                           |

Benchmark hidden because not significant (1): xml_etree_parse

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240605-darwin-arm64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240417-darwin-arm64-python-main-3.13.0a6+-c179c0e |
|------------------------|:----------------------------------------------------------:|:------------------------------------------------------:|
| python_startup_no_site | 12.3 ms                                                    | 9.25 ms: 1.33x faster                                  |
| python_startup         | 15.2 ms                                                    | 12.1 ms: 1.26x faster                                  |
| Geometric mean         | (ref)                                                      | 1.29x faster                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240605-darwin-arm64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240417-darwin-arm64-python-main-3.13.0a6+-c179c0e |
|-----------------|:----------------------------------------------------------:|:------------------------------------------------------:|
| genshi_text     | 13.9 ms                                                    | 15.4 ms: 1.10x slower                                  |
| genshi_xml      | 29.9 ms                                                    | 33.6 ms: 1.12x slower                                  |
| django_template | 19.4 ms                                                    | 23.2 ms: 1.20x slower                                  |
| mako            | 6.99 ms                                                    | 10.5 ms: 1.51x slower                                  |
| Geometric mean  | (ref)                                                      | 1.22x slower                                           |

All benchmarks:
===============

| Benchmark                        | bm-20240605-darwin-arm64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240417-darwin-arm64-python-main-3.13.0a6+-c179c0e |
|----------------------------------|:----------------------------------------------------------:|:------------------------------------------------------:|
| python_startup_no_site           | 12.3 ms                                                    | 9.25 ms: 1.33x faster                                  |
| python_startup                   | 15.2 ms                                                    | 12.1 ms: 1.26x faster                                  |
| typing_runtime_protocols         | 87.6 us                                                    | 73.5 us: 1.19x faster                                  |
| bench_mp_pool                    | 47.2 ms                                                    | 43.7 ms: 1.08x faster                                  |
| create_gc_cycles                 | 897 us                                                     | 870 us: 1.03x faster                                   |
| pickle_dict                      | 18.3 us                                                    | 18.2 us: 1.00x faster                                  |
| gc_traversal                     | 2.45 ms                                                    | 2.45 ms: 1.00x faster                                  |
| asyncio_websockets               | 409 ms                                                     | 408 ms: 1.00x faster                                   |
| pickle                           | 7.48 us                                                    | 7.51 us: 1.00x slower                                  |
| json_dumps                       | 6.23 ms                                                    | 6.27 ms: 1.01x slower                                  |
| json_loads                       | 16.8 us                                                    | 16.9 us: 1.01x slower                                  |
| pidigits                         | 282 ms                                                     | 284 ms: 1.01x slower                                   |
| unpickle_list                    | 2.88 us                                                    | 2.92 us: 1.01x slower                                  |
| pickle_list                      | 2.96 us                                                    | 3.01 us: 1.02x slower                                  |
| unpickle                         | 9.12 us                                                    | 9.29 us: 1.02x slower                                  |
| async_tree_eager_cpu_io_mixed_tg | 331 ms                                                     | 338 ms: 1.02x slower                                   |
| thrift                           | 435 us                                                     | 446 us: 1.02x slower                                   |
| asyncio_tcp_ssl                  | 1.29 sec                                                   | 1.32 sec: 1.03x slower                                 |
| regex_v8                         | 17.3 ms                                                    | 17.8 ms: 1.03x slower                                  |
| async_tree_none                  | 209 ms                                                     | 216 ms: 1.03x slower                                   |
| async_tree_eager_cpu_io_mixed    | 358 ms                                                     | 370 ms: 1.03x slower                                   |
| coverage                         | 45.0 ms                                                    | 46.6 ms: 1.04x slower                                  |
| pickle_pure_python               | 179 us                                                     | 186 us: 1.04x slower                                   |
| async_tree_io                    | 563 ms                                                     | 586 ms: 1.04x slower                                   |
| async_tree_eager_io              | 766 ms                                                     | 798 ms: 1.04x slower                                   |
| pathlib                          | 23.3 ms                                                    | 24.4 ms: 1.05x slower                                  |
| async_tree_eager_memoization     | 152 ms                                                     | 160 ms: 1.05x slower                                   |
| async_tree_none_tg               | 198 ms                                                     | 208 ms: 1.05x slower                                   |
| async_tree_cpu_io_mixed_tg       | 451 ms                                                     | 475 ms: 1.05x slower                                   |
| html5lib                         | 31.2 ms                                                    | 33.0 ms: 1.06x slower                                  |
| deepcopy_reduce                  | 1.82 us                                                    | 1.93 us: 1.06x slower                                  |
| async_tree_eager_memoization_tg  | 126 ms                                                     | 134 ms: 1.07x slower                                   |
| dulwich_log                      | 27.6 ms                                                    | 29.5 ms: 1.07x slower                                  |
| telco                            | 4.60 ms                                                    | 4.94 ms: 1.07x slower                                  |
| coroutines                       | 15.8 ms                                                    | 17.0 ms: 1.08x slower                                  |
| sqlite_synth                     | 1.55 us                                                    | 1.67 us: 1.08x slower                                  |
| logging_format                   | 3.31 us                                                    | 3.57 us: 1.08x slower                                  |
| logging_simple                   | 3.04 us                                                    | 3.29 us: 1.08x slower                                  |
| mdp                              | 1.53 sec                                                   | 1.67 sec: 1.09x slower                                 |
| pylint                           | 170 ms                                                     | 185 ms: 1.09x slower                                   |
| async_generators                 | 281 ms                                                     | 306 ms: 1.09x slower                                   |
| pycparser                        | 632 ms                                                     | 693 ms: 1.10x slower                                   |
| async_tree_memoization           | 260 ms                                                     | 284 ms: 1.10x slower                                   |
| xml_etree_process                | 37.1 ms                                                    | 40.7 ms: 1.10x slower                                  |
| deepcopy                         | 204 us                                                     | 224 us: 1.10x slower                                   |
| mypy2                            | 379 ms                                                     | 418 ms: 1.10x slower                                   |
| genshi_text                      | 13.9 ms                                                    | 15.4 ms: 1.10x slower                                  |
| logging_silent                   | 60.1 ns                                                    | 66.6 ns: 1.11x slower                                  |
| 2to3                             | 161 ms                                                     | 179 ms: 1.11x slower                                   |
| sympy_expand                     | 226 ms                                                     | 251 ms: 1.11x slower                                   |
| docutils                         | 1.44 sec                                                   | 1.61 sec: 1.12x slower                                 |
| genshi_xml                       | 29.9 ms                                                    | 33.6 ms: 1.12x slower                                  |
| xml_etree_generate               | 52.7 ms                                                    | 59.4 ms: 1.13x slower                                  |
| chameleon                        | 4.27 ms                                                    | 4.81 ms: 1.13x slower                                  |
| async_tree_memoization_tg        | 240 ms                                                     | 271 ms: 1.13x slower                                   |
| xml_etree_iterparse              | 71.5 ms                                                    | 80.9 ms: 1.13x slower                                  |
| sqlglot_normalize                | 166 ms                                                     | 188 ms: 1.13x slower                                   |
| async_tree_eager_tg              | 41.4 ms                                                    | 47.0 ms: 1.14x slower                                  |
| aiohttp                          | 997 us                                                     | 1.15 ms: 1.15x slower                                  |
| bench_thread_pool                | 447 us                                                     | 517 us: 1.16x slower                                   |
| gunicorn                         | 1.04 ms                                                    | 1.20 ms: 1.16x slower                                  |
| sqlglot_transpile                | 891 us                                                     | 1.04 ms: 1.17x slower                                  |
| async_tree_eager                 | 60.3 ms                                                    | 71.4 ms: 1.18x slower                                  |
| sqlglot_parse                    | 732 us                                                     | 868 us: 1.19x slower                                   |
| generators                       | 22.9 ms                                                    | 27.2 ms: 1.19x slower                                  |
| sqlglot_optimize                 | 30.9 ms                                                    | 36.8 ms: 1.19x slower                                  |
| django_template                  | 19.4 ms                                                    | 23.2 ms: 1.20x slower                                  |
| sympy_integrate                  | 10.3 ms                                                    | 12.4 ms: 1.20x slower                                  |
| meteor_contest                   | 70.3 ms                                                    | 84.9 ms: 1.21x slower                                  |
| sympy_str                        | 131 ms                                                     | 159 ms: 1.21x slower                                   |
| sympy_sum                        | 69.2 ms                                                    | 84.7 ms: 1.22x slower                                  |
| scimark_sor                      | 94.9 ms                                                    | 117 ms: 1.24x slower                                   |
| richards_super                   | 35.2 ms                                                    | 43.6 ms: 1.24x slower                                  |
| tomli_loads                      | 1.47 sec                                                   | 1.83 sec: 1.25x slower                                 |
| richards                         | 31.8 ms                                                    | 40.2 ms: 1.26x slower                                  |
| tornado_http                     | 66.7 ms                                                    | 84.3 ms: 1.26x slower                                  |
| crypto_pyaes                     | 49.5 ms                                                    | 62.8 ms: 1.27x slower                                  |
| deepcopy_memo                    | 22.6 us                                                    | 28.7 us: 1.27x slower                                  |
| go                               | 101 ms                                                     | 129 ms: 1.28x slower                                   |
| raytrace                         | 147 ms                                                     | 192 ms: 1.31x slower                                   |
| pprint_safe_repr                 | 465 ms                                                     | 645 ms: 1.39x slower                                   |
| pprint_pformat                   | 947 ms                                                     | 1.33 sec: 1.40x slower                                 |
| deltablue                        | 2.14 ms                                                    | 3.03 ms: 1.42x slower                                  |
| unpickle_pure_python             | 141 us                                                     | 202 us: 1.43x slower                                   |
| pyflate                          | 321 ms                                                     | 472 ms: 1.47x slower                                   |
| regex_compile                    | 68.5 ms                                                    | 102 ms: 1.49x slower                                   |
| mako                             | 6.99 ms                                                    | 10.5 ms: 1.51x slower                                  |
| scimark_fft                      | 181 ms                                                     | 275 ms: 1.52x slower                                   |
| chaos                            | 34.0 ms                                                    | 51.8 ms: 1.52x slower                                  |
| nqueens                          | 52.2 ms                                                    | 80.0 ms: 1.53x slower                                  |
| fannkuch                         | 248 ms                                                     | 381 ms: 1.53x slower                                   |
| float                            | 48.6 ms                                                    | 75.1 ms: 1.55x slower                                  |
| nbody                            | 59.6 ms                                                    | 97.8 ms: 1.64x slower                                  |
| scimark_sparse_mat_mult          | 2.77 ms                                                    | 4.60 ms: 1.66x slower                                  |
| scimark_lu                       | 66.9 ms                                                    | 111 ms: 1.66x slower                                   |
| scimark_monte_carlo              | 42.5 ms                                                    | 71.6 ms: 1.69x slower                                  |
| hexiom                           | 4.06 ms                                                    | 7.01 ms: 1.73x slower                                  |
| spectral_norm                    | 66.4 ms                                                    | 116 ms: 1.75x slower                                   |
| comprehensions                   | 10.2 us                                                    | 19.3 us: 1.90x slower                                  |
| Geometric mean                   | (ref)                                                      | 1.15x slower                                           |

Benchmark hidden because not significant (9): regex_dna, regex_effbot, json, xml_etree_parse, async_tree_eager_io_tg, dask, async_tree_cpu_io_mixed, async_tree_io_tg, asyncio_tcp
Ignored benchmarks (2) of results/bm-20240605-3.13.0b2-3a83b17/bm-20240605-darwin-arm64-python-v3.13.0b2-3.13.0b2-3a83b17.json: bpe_tokeniser, flaskblogging

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.10x
- 95% likely to have a slowdown of 1.09x
- 99% likely to have a slowdown of 1.09x

# Memory
- memory change: 0.97x