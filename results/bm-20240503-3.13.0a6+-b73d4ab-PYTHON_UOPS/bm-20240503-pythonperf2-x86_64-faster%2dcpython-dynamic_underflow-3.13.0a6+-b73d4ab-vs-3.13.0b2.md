# Results vs. 3.13.0b2

- fork: faster-cpython
- ref: dynamic_underflow
- machine: linux-x86_64
- commit hash: b73d4ab
- commit date: 2024-05-03
- overall geometric mean: 1.21x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.12x slower
- Memory change: 1.00x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240605-pythonperf2-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240503-pythonperf2-x86_64-faster%2dcpython-dynamic_underflow-3.13.0a6+-b73d4ab |
|----------------|:----------------------------------------------------------------:|:-----------------------------------------------------------------------------------:|
| chameleon      | 7.40 ms                                                          | 8.91 ms: 1.20x slower                                                               |
| tornado_http   | 119 ms                                                           | 139 ms: 1.17x slower                                                                |
| Geometric mean | (ref)                                                            | 1.19x slower                                                                        |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240605-pythonperf2-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240503-pythonperf2-x86_64-faster%2dcpython-dynamic_underflow-3.13.0a6+-b73d4ab |
|----------------------------|:----------------------------------------------------------------:|:-----------------------------------------------------------------------------------:|
| async_tree_io_tg           | 900 ms                                                           | 922 ms: 1.02x slower                                                                |
| async_tree_io              | 873 ms                                                           | 921 ms: 1.05x slower                                                                |
| async_tree_none_tg         | 340 ms                                                           | 363 ms: 1.07x slower                                                                |
| async_tree_memoization_tg  | 421 ms                                                           | 451 ms: 1.07x slower                                                                |
| async_tree_cpu_io_mixed    | 604 ms                                                           | 649 ms: 1.07x slower                                                                |
| async_tree_cpu_io_mixed_tg | 573 ms                                                           | 618 ms: 1.08x slower                                                                |
| async_tree_none            | 365 ms                                                           | 399 ms: 1.09x slower                                                                |
| async_tree_memoization     | 460 ms                                                           | 502 ms: 1.09x slower                                                                |
| Geometric mean             | (ref)                                                            | 1.07x slower                                                                        |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240605-pythonperf2-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240503-pythonperf2-x86_64-faster%2dcpython-dynamic_underflow-3.13.0a6+-b73d4ab |
|----------------|:----------------------------------------------------------------:|:-----------------------------------------------------------------------------------:|
| pidigits       | 254 ms                                                           | 256 ms: 1.01x slower                                                                |
| float          | 80.2 ms                                                          | 98.7 ms: 1.23x slower                                                               |
| nbody          | 87.8 ms                                                          | 129 ms: 1.47x slower                                                                |
| Geometric mean | (ref)                                                            | 1.22x slower                                                                        |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240605-pythonperf2-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240503-pythonperf2-x86_64-faster%2dcpython-dynamic_underflow-3.13.0a6+-b73d4ab |
|----------------|:----------------------------------------------------------------:|:-----------------------------------------------------------------------------------:|
| regex_dna      | 249 ms                                                           | 242 ms: 1.03x faster                                                                |
| regex_v8       | 26.0 ms                                                          | 26.3 ms: 1.01x slower                                                               |
| regex_effbot   | 3.40 ms                                                          | 3.52 ms: 1.04x slower                                                               |
| regex_compile  | 144 ms                                                           | 231 ms: 1.60x slower                                                                |
| Geometric mean | (ref)                                                            | 1.13x slower                                                                        |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240605-pythonperf2-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240503-pythonperf2-x86_64-faster%2dcpython-dynamic_underflow-3.13.0a6+-b73d4ab |
|----------------------|:----------------------------------------------------------------:|:-----------------------------------------------------------------------------------:|
| unpickle             | 15.7 us                                                          | 15.2 us: 1.03x faster                                                               |
| pickle_list          | 4.44 us                                                          | 4.37 us: 1.02x faster                                                               |
| pickle_dict          | 32.8 us                                                          | 32.7 us: 1.01x faster                                                               |
| pickle               | 10.6 us                                                          | 10.7 us: 1.01x slower                                                               |
| xml_etree_parse      | 144 ms                                                           | 146 ms: 1.02x slower                                                                |
| unpickle_list        | 4.70 us                                                          | 4.80 us: 1.02x slower                                                               |
| json_dumps           | 10.8 ms                                                          | 11.4 ms: 1.06x slower                                                               |
| xml_etree_iterparse  | 103 ms                                                           | 116 ms: 1.13x slower                                                                |
| xml_etree_generate   | 85.7 ms                                                          | 97.6 ms: 1.14x slower                                                               |
| xml_etree_process    | 59.7 ms                                                          | 69.2 ms: 1.16x slower                                                               |
| tomli_loads          | 2.40 sec                                                         | 3.32 sec: 1.38x slower                                                              |
| unpickle_pure_python | 224 us                                                           | 335 us: 1.49x slower                                                                |
| pickle_pure_python   | 307 us                                                           | 479 us: 1.56x slower                                                                |
| Geometric mean       | (ref)                                                            | 1.12x slower                                                                        |

Benchmark hidden because not significant (1): json_loads

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240605-pythonperf2-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240503-pythonperf2-x86_64-faster%2dcpython-dynamic_underflow-3.13.0a6+-b73d4ab |
|------------------------|:----------------------------------------------------------------:|:-----------------------------------------------------------------------------------:|
| python_startup         | 13.2 ms                                                          | 13.0 ms: 1.02x faster                                                               |
| python_startup_no_site | 8.85 ms                                                          | 8.93 ms: 1.01x slower                                                               |
| Geometric mean         | (ref)                                                            | 1.00x faster                                                                        |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240605-pythonperf2-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240503-pythonperf2-x86_64-faster%2dcpython-dynamic_underflow-3.13.0a6+-b73d4ab |
|-----------------|:----------------------------------------------------------------:|:-----------------------------------------------------------------------------------:|
| django_template | 39.0 ms                                                          | 46.8 ms: 1.20x slower                                                               |
| mako            | 10.4 ms                                                          | 14.2 ms: 1.37x slower                                                               |
| Geometric mean  | (ref)                                                            | 1.28x slower                                                                        |

All benchmarks:
===============

| Benchmark                  | bm-20240605-pythonperf2-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240503-pythonperf2-x86_64-faster%2dcpython-dynamic_underflow-3.13.0a6+-b73d4ab |
|----------------------------|:----------------------------------------------------------------:|:-----------------------------------------------------------------------------------:|
| gc_traversal               | 4.69 ms                                                          | 4.47 ms: 1.05x faster                                                               |
| regex_dna                  | 249 ms                                                           | 242 ms: 1.03x faster                                                                |
| unpickle                   | 15.7 us                                                          | 15.2 us: 1.03x faster                                                               |
| coverage                   | 83.5 ms                                                          | 81.6 ms: 1.02x faster                                                               |
| pickle_list                | 4.44 us                                                          | 4.37 us: 1.02x faster                                                               |
| python_startup             | 13.2 ms                                                          | 13.0 ms: 1.02x faster                                                               |
| asyncio_websockets         | 395 ms                                                           | 390 ms: 1.01x faster                                                                |
| pickle_dict                | 32.8 us                                                          | 32.7 us: 1.01x faster                                                               |
| pidigits                   | 254 ms                                                           | 256 ms: 1.01x slower                                                                |
| python_startup_no_site     | 8.85 ms                                                          | 8.93 ms: 1.01x slower                                                               |
| pickle                     | 10.6 us                                                          | 10.7 us: 1.01x slower                                                               |
| regex_v8                   | 26.0 ms                                                          | 26.3 ms: 1.01x slower                                                               |
| xml_etree_parse            | 144 ms                                                           | 146 ms: 1.02x slower                                                                |
| asyncio_tcp_ssl            | 1.58 sec                                                         | 1.61 sec: 1.02x slower                                                              |
| generators                 | 33.5 ms                                                          | 34.2 ms: 1.02x slower                                                               |
| unpickle_list              | 4.70 us                                                          | 4.80 us: 1.02x slower                                                               |
| coroutines                 | 22.0 ms                                                          | 22.5 ms: 1.02x slower                                                               |
| async_tree_io_tg           | 900 ms                                                           | 922 ms: 1.02x slower                                                                |
| json                       | 5.35 ms                                                          | 5.53 ms: 1.03x slower                                                               |
| regex_effbot               | 3.40 ms                                                          | 3.52 ms: 1.04x slower                                                               |
| asyncio_tcp                | 378 ms                                                           | 392 ms: 1.04x slower                                                                |
| logging_format             | 7.11 us                                                          | 7.50 us: 1.05x slower                                                               |
| async_tree_io              | 873 ms                                                           | 921 ms: 1.05x slower                                                                |
| sqlite_synth               | 2.80 us                                                          | 2.95 us: 1.06x slower                                                               |
| json_dumps                 | 10.8 ms                                                          | 11.4 ms: 1.06x slower                                                               |
| thrift                     | 880 us                                                           | 934 us: 1.06x slower                                                                |
| logging_simple             | 6.40 us                                                          | 6.81 us: 1.06x slower                                                               |
| async_tree_none_tg         | 340 ms                                                           | 363 ms: 1.07x slower                                                                |
| async_tree_memoization_tg  | 421 ms                                                           | 451 ms: 1.07x slower                                                                |
| async_tree_cpu_io_mixed    | 604 ms                                                           | 649 ms: 1.07x slower                                                                |
| async_tree_cpu_io_mixed_tg | 573 ms                                                           | 618 ms: 1.08x slower                                                                |
| pathlib                    | 17.1 ms                                                          | 18.5 ms: 1.08x slower                                                               |
| async_tree_none            | 365 ms                                                           | 399 ms: 1.09x slower                                                                |
| async_tree_memoization     | 460 ms                                                           | 502 ms: 1.09x slower                                                                |
| async_generators           | 363 ms                                                           | 398 ms: 1.10x slower                                                                |
| flaskblogging              | 4.68 ms                                                          | 5.19 ms: 1.11x slower                                                               |
| telco                      | 8.40 ms                                                          | 9.35 ms: 1.11x slower                                                               |
| mdp                        | 2.46 sec                                                         | 2.77 sec: 1.13x slower                                                              |
| dask                       | 391 ms                                                           | 441 ms: 1.13x slower                                                                |
| xml_etree_iterparse        | 103 ms                                                           | 116 ms: 1.13x slower                                                                |
| xml_etree_generate         | 85.7 ms                                                          | 97.6 ms: 1.14x slower                                                               |
| meteor_contest             | 128 ms                                                           | 148 ms: 1.16x slower                                                                |
| xml_etree_process          | 59.7 ms                                                          | 69.2 ms: 1.16x slower                                                               |
| bench_thread_pool          | 908 us                                                           | 1.05 ms: 1.16x slower                                                               |
| tornado_http               | 119 ms                                                           | 139 ms: 1.17x slower                                                                |
| typing_runtime_protocols   | 171 us                                                           | 204 us: 1.20x slower                                                                |
| django_template            | 39.0 ms                                                          | 46.8 ms: 1.20x slower                                                               |
| chameleon                  | 7.40 ms                                                          | 8.91 ms: 1.20x slower                                                               |
| gunicorn                   | 1.04 ms                                                          | 1.26 ms: 1.21x slower                                                               |
| aiohttp                    | 1.07 ms                                                          | 1.30 ms: 1.21x slower                                                               |
| deepcopy_reduce            | 3.39 us                                                          | 4.14 us: 1.22x slower                                                               |
| float                      | 80.2 ms                                                          | 98.7 ms: 1.23x slower                                                               |
| pycparser                  | 1.22 sec                                                         | 1.51 sec: 1.24x slower                                                              |
| sqlglot_optimize           | 59.5 ms                                                          | 74.3 ms: 1.25x slower                                                               |
| crypto_pyaes               | 73.6 ms                                                          | 92.9 ms: 1.26x slower                                                               |
| sqlglot_parse              | 1.39 ms                                                          | 1.76 ms: 1.26x slower                                                               |
| sqlglot_normalize          | 120 ms                                                           | 153 ms: 1.27x slower                                                                |
| richards_super             | 61.2 ms                                                          | 78.3 ms: 1.28x slower                                                               |
| sqlglot_transpile          | 1.76 ms                                                          | 2.26 ms: 1.28x slower                                                               |
| go                         | 165 ms                                                           | 216 ms: 1.31x slower                                                                |
| deepcopy                   | 377 us                                                           | 495 us: 1.31x slower                                                                |
| pyflate                    | 482 ms                                                           | 632 ms: 1.31x slower                                                                |
| sympy_integrate            | 23.2 ms                                                          | 30.4 ms: 1.31x slower                                                               |
| dulwich_log                | 67.3 ms                                                          | 88.7 ms: 1.32x slower                                                               |
| richards                   | 53.4 ms                                                          | 70.8 ms: 1.32x slower                                                               |
| mypy2                      | 764 ms                                                           | 1.01 sec: 1.33x slower                                                              |
| pylint                     | 339 ms                                                           | 454 ms: 1.34x slower                                                                |
| sympy_sum                  | 155 ms                                                           | 208 ms: 1.34x slower                                                                |
| pprint_safe_repr           | 818 ms                                                           | 1.10 sec: 1.34x slower                                                              |
| pprint_pformat             | 1.66 sec                                                         | 2.25 sec: 1.36x slower                                                              |
| nqueens                    | 88.4 ms                                                          | 120 ms: 1.36x slower                                                                |
| sympy_expand               | 501 ms                                                           | 685 ms: 1.37x slower                                                                |
| mako                       | 10.4 ms                                                          | 14.2 ms: 1.37x slower                                                               |
| tomli_loads                | 2.40 sec                                                         | 3.32 sec: 1.38x slower                                                              |
| sympy_str                  | 295 ms                                                           | 410 ms: 1.39x slower                                                                |
| scimark_fft                | 312 ms                                                           | 437 ms: 1.40x slower                                                                |
| chaos                      | 59.6 ms                                                          | 83.5 ms: 1.40x slower                                                               |
| raytrace                   | 260 ms                                                           | 365 ms: 1.40x slower                                                                |
| scimark_sor                | 119 ms                                                           | 167 ms: 1.40x slower                                                                |
| fannkuch                   | 353 ms                                                           | 498 ms: 1.41x slower                                                                |
| nbody                      | 87.8 ms                                                          | 129 ms: 1.47x slower                                                                |
| unpickle_pure_python       | 224 us                                                           | 335 us: 1.49x slower                                                                |
| spectral_norm              | 97.3 ms                                                          | 146 ms: 1.50x slower                                                                |
| scimark_lu                 | 97.5 ms                                                          | 149 ms: 1.53x slower                                                                |
| pickle_pure_python         | 307 us                                                           | 479 us: 1.56x slower                                                                |
| regex_compile              | 144 ms                                                           | 231 ms: 1.60x slower                                                                |
| scimark_sparse_mat_mult    | 4.28 ms                                                          | 6.92 ms: 1.62x slower                                                               |
| scimark_monte_carlo        | 65.5 ms                                                          | 109 ms: 1.66x slower                                                                |
| deepcopy_memo              | 37.3 us                                                          | 62.1 us: 1.67x slower                                                               |
| comprehensions             | 17.0 us                                                          | 28.3 us: 1.67x slower                                                               |
| hexiom                     | 6.35 ms                                                          | 10.9 ms: 1.72x slower                                                               |
| logging_silent             | 96.3 ns                                                          | 174 ns: 1.81x slower                                                                |
| deltablue                  | 3.37 ms                                                          | 6.33 ms: 1.88x slower                                                               |
| Geometric mean             | (ref)                                                            | 1.21x slower                                                                        |

Benchmark hidden because not significant (3): create_gc_cycles, json_loads, bench_mp_pool
Ignored benchmarks (6) of results/bm-20240605-3.13.0b2-3a83b17/bm-20240605-pythonperf2-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17.json: 2to3, bpe_tokeniser, docutils, genshi_text, genshi_xml, html5lib

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.15x
- 95% likely to have a slowdown of 1.14x
- 99% likely to have a slowdown of 1.12x

# Memory
- memory change: 1.00x