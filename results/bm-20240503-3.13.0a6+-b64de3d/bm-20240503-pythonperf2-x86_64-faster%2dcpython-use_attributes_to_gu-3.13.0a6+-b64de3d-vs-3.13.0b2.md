# Results vs. 3.13.0b2

- fork: faster-cpython
- ref: use_attributes_to_gu
- machine: linux-x86_64
- commit hash: b64de3d
- commit date: 2024-05-03
- overall geometric mean: 1.01x slower
- HPT reliability: 99.81%
- HPT 99th percentile: 1.00x slower
- Memory change: 0.98x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240605-pythonperf2-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240503-pythonperf2-x86_64-faster%2dcpython-use_attributes_to_gu-3.13.0a6+-b64de3d |
|----------------|:----------------------------------------------------------------:|:--------------------------------------------------------------------------------------:|
| 2to3           | 291 ms                                                           | 291 ms: 1.00x faster                                                                   |
| chameleon      | 7.40 ms                                                          | 7.52 ms: 1.02x slower                                                                  |
| docutils       | 2.98 sec                                                         | 3.02 sec: 1.01x slower                                                                 |
| html5lib       | 74.7 ms                                                          | 75.9 ms: 1.02x slower                                                                  |
| Geometric mean | (ref)                                                            | 1.01x slower                                                                           |

Benchmark hidden because not significant (1): tornado_http

Benchmarks with tag 'asyncio':
==============================

| Benchmark                 | bm-20240605-pythonperf2-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240503-pythonperf2-x86_64-faster%2dcpython-use_attributes_to_gu-3.13.0a6+-b64de3d |
|---------------------------|:----------------------------------------------------------------:|:--------------------------------------------------------------------------------------:|
| async_tree_none           | 365 ms                                                           | 376 ms: 1.03x slower                                                                   |
| async_tree_cpu_io_mixed   | 604 ms                                                           | 622 ms: 1.03x slower                                                                   |
| async_tree_memoization    | 460 ms                                                           | 475 ms: 1.03x slower                                                                   |
| async_tree_io             | 873 ms                                                           | 907 ms: 1.04x slower                                                                   |
| async_tree_memoization_tg | 421 ms                                                           | 445 ms: 1.06x slower                                                                   |
| Geometric mean            | (ref)                                                            | 1.03x slower                                                                           |

Benchmark hidden because not significant (3): async_tree_io_tg, async_tree_none_tg, async_tree_cpu_io_mixed_tg

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240605-pythonperf2-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240503-pythonperf2-x86_64-faster%2dcpython-use_attributes_to_gu-3.13.0a6+-b64de3d |
|----------------|:----------------------------------------------------------------:|:--------------------------------------------------------------------------------------:|
| pidigits       | 254 ms                                                           | 255 ms: 1.00x slower                                                                   |
| float          | 80.2 ms                                                          | 80.9 ms: 1.01x slower                                                                  |
| nbody          | 87.8 ms                                                          | 91.0 ms: 1.04x slower                                                                  |
| Geometric mean | (ref)                                                            | 1.02x slower                                                                           |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240605-pythonperf2-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240503-pythonperf2-x86_64-faster%2dcpython-use_attributes_to_gu-3.13.0a6+-b64de3d |
|----------------|:----------------------------------------------------------------:|:--------------------------------------------------------------------------------------:|
| regex_dna      | 249 ms                                                           | 237 ms: 1.05x faster                                                                   |
| regex_v8       | 26.0 ms                                                          | 25.6 ms: 1.02x faster                                                                  |
| regex_compile  | 144 ms                                                           | 143 ms: 1.01x faster                                                                   |
| regex_effbot   | 3.40 ms                                                          | 3.52 ms: 1.04x slower                                                                  |
| Geometric mean | (ref)                                                            | 1.01x faster                                                                           |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240605-pythonperf2-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240503-pythonperf2-x86_64-faster%2dcpython-use_attributes_to_gu-3.13.0a6+-b64de3d |
|----------------------|:----------------------------------------------------------------:|:--------------------------------------------------------------------------------------:|
| unpickle_pure_python | 224 us                                                           | 213 us: 1.05x faster                                                                   |
| unpickle             | 15.7 us                                                          | 15.1 us: 1.04x faster                                                                  |
| json_loads           | 25.0 us                                                          | 24.6 us: 1.02x faster                                                                  |
| xml_etree_generate   | 85.7 ms                                                          | 84.7 ms: 1.01x faster                                                                  |
| xml_etree_process    | 59.7 ms                                                          | 59.1 ms: 1.01x faster                                                                  |
| tomli_loads          | 2.40 sec                                                         | 2.38 sec: 1.01x faster                                                                 |
| xml_etree_iterparse  | 103 ms                                                           | 104 ms: 1.01x slower                                                                   |
| pickle_list          | 4.44 us                                                          | 4.49 us: 1.01x slower                                                                  |
| xml_etree_parse      | 144 ms                                                           | 145 ms: 1.01x slower                                                                   |
| pickle               | 10.6 us                                                          | 10.9 us: 1.02x slower                                                                  |
| json_dumps           | 10.8 ms                                                          | 11.1 ms: 1.03x slower                                                                  |
| pickle_pure_python   | 307 us                                                           | 326 us: 1.06x slower                                                                   |
| Geometric mean       | (ref)                                                            | 1.00x slower                                                                           |

Benchmark hidden because not significant (2): unpickle_list, pickle_dict

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240605-pythonperf2-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240503-pythonperf2-x86_64-faster%2dcpython-use_attributes_to_gu-3.13.0a6+-b64de3d |
|------------------------|:----------------------------------------------------------------:|:--------------------------------------------------------------------------------------:|
| python_startup         | 13.2 ms                                                          | 12.8 ms: 1.03x faster                                                                  |
| python_startup_no_site | 8.85 ms                                                          | 8.80 ms: 1.01x faster                                                                  |
| Geometric mean         | (ref)                                                            | 1.02x faster                                                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240605-pythonperf2-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240503-pythonperf2-x86_64-faster%2dcpython-use_attributes_to_gu-3.13.0a6+-b64de3d |
|-----------------|:----------------------------------------------------------------:|:--------------------------------------------------------------------------------------:|
| genshi_xml      | 58.1 ms                                                          | 53.3 ms: 1.09x faster                                                                  |
| genshi_text     | 25.9 ms                                                          | 24.8 ms: 1.05x faster                                                                  |
| django_template | 39.0 ms                                                          | 39.6 ms: 1.02x slower                                                                  |
| Geometric mean  | (ref)                                                            | 1.03x faster                                                                           |

Benchmark hidden because not significant (1): mako

All benchmarks:
===============

| Benchmark                 | bm-20240605-pythonperf2-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240503-pythonperf2-x86_64-faster%2dcpython-use_attributes_to_gu-3.13.0a6+-b64de3d |
|---------------------------|:----------------------------------------------------------------:|:--------------------------------------------------------------------------------------:|
| go                        | 165 ms                                                           | 134 ms: 1.23x faster                                                                   |
| genshi_xml                | 58.1 ms                                                          | 53.3 ms: 1.09x faster                                                                  |
| coverage                  | 83.5 ms                                                          | 77.4 ms: 1.08x faster                                                                  |
| bench_mp_pool             | 4.91 ms                                                          | 4.66 ms: 1.05x faster                                                                  |
| unpickle_pure_python      | 224 us                                                           | 213 us: 1.05x faster                                                                   |
| regex_dna                 | 249 ms                                                           | 237 ms: 1.05x faster                                                                   |
| genshi_text               | 25.9 ms                                                          | 24.8 ms: 1.05x faster                                                                  |
| richards                  | 53.4 ms                                                          | 51.2 ms: 1.04x faster                                                                  |
| richards_super            | 61.2 ms                                                          | 58.8 ms: 1.04x faster                                                                  |
| unpickle                  | 15.7 us                                                          | 15.1 us: 1.04x faster                                                                  |
| python_startup            | 13.2 ms                                                          | 12.8 ms: 1.03x faster                                                                  |
| coroutines                | 22.0 ms                                                          | 21.5 ms: 1.02x faster                                                                  |
| regex_v8                  | 26.0 ms                                                          | 25.6 ms: 1.02x faster                                                                  |
| json_loads                | 25.0 us                                                          | 24.6 us: 1.02x faster                                                                  |
| pyflate                   | 482 ms                                                           | 474 ms: 1.02x faster                                                                   |
| dulwich_log               | 67.3 ms                                                          | 66.2 ms: 1.02x faster                                                                  |
| telco                     | 8.40 ms                                                          | 8.27 ms: 1.02x faster                                                                  |
| asyncio_tcp               | 378 ms                                                           | 373 ms: 1.01x faster                                                                   |
| xml_etree_generate        | 85.7 ms                                                          | 84.7 ms: 1.01x faster                                                                  |
| xml_etree_process         | 59.7 ms                                                          | 59.1 ms: 1.01x faster                                                                  |
| tomli_loads               | 2.40 sec                                                         | 2.38 sec: 1.01x faster                                                                 |
| regex_compile             | 144 ms                                                           | 143 ms: 1.01x faster                                                                   |
| python_startup_no_site    | 8.85 ms                                                          | 8.80 ms: 1.01x faster                                                                  |
| pprint_safe_repr          | 818 ms                                                           | 814 ms: 1.00x faster                                                                   |
| 2to3                      | 291 ms                                                           | 291 ms: 1.00x faster                                                                   |
| asyncio_tcp_ssl           | 1.58 sec                                                         | 1.58 sec: 1.00x faster                                                                 |
| generators                | 33.5 ms                                                          | 33.6 ms: 1.00x slower                                                                  |
| hexiom                    | 6.35 ms                                                          | 6.38 ms: 1.00x slower                                                                  |
| pidigits                  | 254 ms                                                           | 255 ms: 1.00x slower                                                                   |
| deepcopy_memo             | 37.3 us                                                          | 37.5 us: 1.01x slower                                                                  |
| sqlglot_transpile         | 1.76 ms                                                          | 1.78 ms: 1.01x slower                                                                  |
| comprehensions            | 17.0 us                                                          | 17.1 us: 1.01x slower                                                                  |
| float                     | 80.2 ms                                                          | 80.9 ms: 1.01x slower                                                                  |
| sqlglot_optimize          | 59.5 ms                                                          | 60.1 ms: 1.01x slower                                                                  |
| sqlite_synth              | 2.80 us                                                          | 2.82 us: 1.01x slower                                                                  |
| xml_etree_iterparse       | 103 ms                                                           | 104 ms: 1.01x slower                                                                   |
| pickle_list               | 4.44 us                                                          | 4.49 us: 1.01x slower                                                                  |
| sqlglot_normalize         | 120 ms                                                           | 122 ms: 1.01x slower                                                                   |
| sympy_expand              | 501 ms                                                           | 506 ms: 1.01x slower                                                                   |
| xml_etree_parse           | 144 ms                                                           | 145 ms: 1.01x slower                                                                   |
| deepcopy_reduce           | 3.39 us                                                          | 3.43 us: 1.01x slower                                                                  |
| sympy_integrate           | 23.2 ms                                                          | 23.4 ms: 1.01x slower                                                                  |
| sympy_str                 | 295 ms                                                           | 298 ms: 1.01x slower                                                                   |
| docutils                  | 2.98 sec                                                         | 3.02 sec: 1.01x slower                                                                 |
| flaskblogging             | 4.68 ms                                                          | 4.75 ms: 1.01x slower                                                                  |
| async_generators          | 363 ms                                                           | 368 ms: 1.02x slower                                                                   |
| django_template           | 39.0 ms                                                          | 39.6 ms: 1.02x slower                                                                  |
| mdp                       | 2.46 sec                                                         | 2.50 sec: 1.02x slower                                                                 |
| aiohttp                   | 1.07 ms                                                          | 1.09 ms: 1.02x slower                                                                  |
| chameleon                 | 7.40 ms                                                          | 7.52 ms: 1.02x slower                                                                  |
| html5lib                  | 74.7 ms                                                          | 75.9 ms: 1.02x slower                                                                  |
| mypy2                     | 764 ms                                                           | 778 ms: 1.02x slower                                                                   |
| logging_silent            | 96.3 ns                                                          | 98.0 ns: 1.02x slower                                                                  |
| meteor_contest            | 128 ms                                                           | 131 ms: 1.02x slower                                                                   |
| pathlib                   | 17.1 ms                                                          | 17.5 ms: 1.02x slower                                                                  |
| scimark_lu                | 97.5 ms                                                          | 99.5 ms: 1.02x slower                                                                  |
| thrift                    | 880 us                                                           | 898 us: 1.02x slower                                                                   |
| nqueens                   | 88.4 ms                                                          | 90.2 ms: 1.02x slower                                                                  |
| typing_runtime_protocols  | 171 us                                                           | 175 us: 1.02x slower                                                                   |
| deltablue                 | 3.37 ms                                                          | 3.46 ms: 1.02x slower                                                                  |
| pickle                    | 10.6 us                                                          | 10.9 us: 1.02x slower                                                                  |
| fannkuch                  | 353 ms                                                           | 362 ms: 1.03x slower                                                                   |
| gc_traversal              | 4.69 ms                                                          | 4.82 ms: 1.03x slower                                                                  |
| async_tree_none           | 365 ms                                                           | 376 ms: 1.03x slower                                                                   |
| pycparser                 | 1.22 sec                                                         | 1.26 sec: 1.03x slower                                                                 |
| json_dumps                | 10.8 ms                                                          | 11.1 ms: 1.03x slower                                                                  |
| async_tree_cpu_io_mixed   | 604 ms                                                           | 622 ms: 1.03x slower                                                                   |
| async_tree_memoization    | 460 ms                                                           | 475 ms: 1.03x slower                                                                   |
| nbody                     | 87.8 ms                                                          | 91.0 ms: 1.04x slower                                                                  |
| spectral_norm             | 97.3 ms                                                          | 101 ms: 1.04x slower                                                                   |
| regex_effbot              | 3.40 ms                                                          | 3.52 ms: 1.04x slower                                                                  |
| raytrace                  | 260 ms                                                           | 270 ms: 1.04x slower                                                                   |
| async_tree_io             | 873 ms                                                           | 907 ms: 1.04x slower                                                                   |
| chaos                     | 59.6 ms                                                          | 62.1 ms: 1.04x slower                                                                  |
| async_tree_memoization_tg | 421 ms                                                           | 445 ms: 1.06x slower                                                                   |
| pickle_pure_python        | 307 us                                                           | 326 us: 1.06x slower                                                                   |
| logging_simple            | 6.40 us                                                          | 6.81 us: 1.06x slower                                                                  |
| logging_format            | 7.11 us                                                          | 7.67 us: 1.08x slower                                                                  |
| scimark_sor               | 119 ms                                                           | 130 ms: 1.09x slower                                                                   |
| crypto_pyaes              | 73.6 ms                                                          | 82.0 ms: 1.11x slower                                                                  |
| scimark_monte_carlo       | 65.5 ms                                                          | 73.8 ms: 1.13x slower                                                                  |
| Geometric mean            | (ref)                                                            | 1.01x slower                                                                           |

Benchmark hidden because not significant (20): bench_thread_pool, unpickle_list, sympy_sum, tornado_http, asyncio_websockets, scimark_sparse_mat_mult, deepcopy, sqlglot_parse, pprint_pformat, pickle_dict, create_gc_cycles, gunicorn, dask, json, mako, async_tree_io_tg, scimark_fft, pylint, async_tree_none_tg, async_tree_cpu_io_mixed_tg
Ignored benchmarks (1) of results/bm-20240605-3.13.0b2-3a83b17/bm-20240605-pythonperf2-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17.json: bpe_tokeniser

# HPT report

- Reliability score: 99.81% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 0.98x