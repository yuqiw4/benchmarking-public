# Results vs. 3.13.0b2

- fork: mdboom
- ref: dont_inline
- machine: linux-x86_64
- commit hash: c35ee28
- commit date: 2024-04-04
- overall geometric mean: 1.02x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.01x slower
- Memory change: 1.06x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240605-pythonperf2-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240404-pythonperf2-x86_64-mdboom-dont_inline-3.13.0a5+-c35ee28 |
|----------------|:----------------------------------------------------------------:|:-------------------------------------------------------------------:|
| 2to3           | 291 ms                                                           | 298 ms: 1.02x slower                                                |
| chameleon      | 7.40 ms                                                          | 7.46 ms: 1.01x slower                                               |
| docutils       | 2.98 sec                                                         | 3.10 sec: 1.04x slower                                              |
| html5lib       | 74.7 ms                                                          | 72.5 ms: 1.03x faster                                               |
| tornado_http   | 119 ms                                                           | 122 ms: 1.02x slower                                                |
| Geometric mean | (ref)                                                            | 1.01x slower                                                        |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240605-pythonperf2-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240404-pythonperf2-x86_64-mdboom-dont_inline-3.13.0a5+-c35ee28 |
|----------------------------|:----------------------------------------------------------------:|:-------------------------------------------------------------------:|
| async_tree_io_tg           | 900 ms                                                           | 864 ms: 1.04x faster                                                |
| async_tree_io              | 873 ms                                                           | 856 ms: 1.02x faster                                                |
| async_tree_cpu_io_mixed_tg | 573 ms                                                           | 592 ms: 1.03x slower                                                |
| async_tree_none            | 365 ms                                                           | 379 ms: 1.04x slower                                                |
| Geometric mean             | (ref)                                                            | 1.00x faster                                                        |

Benchmark hidden because not significant (4): async_tree_memoization, async_tree_none_tg, async_tree_cpu_io_mixed, async_tree_memoization_tg

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240605-pythonperf2-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240404-pythonperf2-x86_64-mdboom-dont_inline-3.13.0a5+-c35ee28 |
|----------------|:----------------------------------------------------------------:|:-------------------------------------------------------------------:|
| float          | 80.2 ms                                                          | 75.0 ms: 1.07x faster                                               |
| pidigits       | 254 ms                                                           | 261 ms: 1.03x slower                                                |
| nbody          | 87.8 ms                                                          | 95.1 ms: 1.08x slower                                               |
| Geometric mean | (ref)                                                            | 1.01x slower                                                        |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240605-pythonperf2-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240404-pythonperf2-x86_64-mdboom-dont_inline-3.13.0a5+-c35ee28 |
|----------------|:----------------------------------------------------------------:|:-------------------------------------------------------------------:|
| regex_dna      | 249 ms                                                           | 241 ms: 1.04x faster                                                |
| regex_v8       | 26.0 ms                                                          | 26.0 ms: 1.00x faster                                               |
| regex_compile  | 144 ms                                                           | 148 ms: 1.03x slower                                                |
| regex_effbot   | 3.40 ms                                                          | 3.52 ms: 1.03x slower                                               |
| Geometric mean | (ref)                                                            | 1.01x slower                                                        |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240605-pythonperf2-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240404-pythonperf2-x86_64-mdboom-dont_inline-3.13.0a5+-c35ee28 |
|----------------------|:----------------------------------------------------------------:|:-------------------------------------------------------------------:|
| tomli_loads          | 2.40 sec                                                         | 2.16 sec: 1.11x faster                                              |
| unpickle_list        | 4.70 us                                                          | 4.54 us: 1.03x faster                                               |
| unpickle             | 15.7 us                                                          | 15.2 us: 1.03x faster                                               |
| xml_etree_process    | 59.7 ms                                                          | 57.9 ms: 1.03x faster                                               |
| xml_etree_generate   | 85.7 ms                                                          | 83.4 ms: 1.03x faster                                               |
| json_dumps           | 10.8 ms                                                          | 10.6 ms: 1.02x faster                                               |
| pickle_dict          | 32.8 us                                                          | 32.7 us: 1.00x faster                                               |
| pickle_pure_python   | 307 us                                                           | 309 us: 1.01x slower                                                |
| xml_etree_iterparse  | 103 ms                                                           | 103 ms: 1.01x slower                                                |
| pickle               | 10.6 us                                                          | 10.7 us: 1.01x slower                                               |
| xml_etree_parse      | 144 ms                                                           | 146 ms: 1.02x slower                                                |
| json_loads           | 25.0 us                                                          | 25.5 us: 1.02x slower                                               |
| unpickle_pure_python | 224 us                                                           | 234 us: 1.04x slower                                                |
| Geometric mean       | (ref)                                                            | 1.01x faster                                                        |

Benchmark hidden because not significant (1): pickle_list

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240605-pythonperf2-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240404-pythonperf2-x86_64-mdboom-dont_inline-3.13.0a5+-c35ee28 |
|------------------------|:----------------------------------------------------------------:|:-------------------------------------------------------------------:|
| python_startup         | 13.2 ms                                                          | 13.5 ms: 1.02x slower                                               |
| python_startup_no_site | 8.85 ms                                                          | 11.8 ms: 1.33x slower                                               |
| Geometric mean         | (ref)                                                            | 1.16x slower                                                        |

Benchmarks with tag 'template':
===============================

| Benchmark      | bm-20240605-pythonperf2-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240404-pythonperf2-x86_64-mdboom-dont_inline-3.13.0a5+-c35ee28 |
|----------------|:----------------------------------------------------------------:|:-------------------------------------------------------------------:|
| mako           | 10.4 ms                                                          | 9.85 ms: 1.05x faster                                               |
| genshi_text    | 25.9 ms                                                          | 26.4 ms: 1.02x slower                                               |
| Geometric mean | (ref)                                                            | 1.01x faster                                                        |

Benchmark hidden because not significant (1): genshi_xml

All benchmarks:
===============

| Benchmark                  | bm-20240605-pythonperf2-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240404-pythonperf2-x86_64-mdboom-dont_inline-3.13.0a5+-c35ee28 |
|----------------------------|:----------------------------------------------------------------:|:-------------------------------------------------------------------:|
| typing_runtime_protocols   | 171 us                                                           | 120 us: 1.42x faster                                                |
| tomli_loads                | 2.40 sec                                                         | 2.16 sec: 1.11x faster                                              |
| create_gc_cycles           | 2.00 ms                                                          | 1.86 ms: 1.08x faster                                               |
| richards_super             | 61.2 ms                                                          | 57.0 ms: 1.07x faster                                               |
| float                      | 80.2 ms                                                          | 75.0 ms: 1.07x faster                                               |
| gc_traversal               | 4.69 ms                                                          | 4.41 ms: 1.06x faster                                               |
| mako                       | 10.4 ms                                                          | 9.85 ms: 1.05x faster                                               |
| richards                   | 53.4 ms                                                          | 50.8 ms: 1.05x faster                                               |
| telco                      | 8.40 ms                                                          | 8.01 ms: 1.05x faster                                               |
| sqlite_synth               | 2.80 us                                                          | 2.68 us: 1.04x faster                                               |
| async_tree_io_tg           | 900 ms                                                           | 864 ms: 1.04x faster                                                |
| spectral_norm              | 97.3 ms                                                          | 93.7 ms: 1.04x faster                                               |
| scimark_sparse_mat_mult    | 4.28 ms                                                          | 4.13 ms: 1.04x faster                                               |
| regex_dna                  | 249 ms                                                           | 241 ms: 1.04x faster                                                |
| unpickle_list              | 4.70 us                                                          | 4.54 us: 1.03x faster                                               |
| unpickle                   | 15.7 us                                                          | 15.2 us: 1.03x faster                                               |
| xml_etree_process          | 59.7 ms                                                          | 57.9 ms: 1.03x faster                                               |
| html5lib                   | 74.7 ms                                                          | 72.5 ms: 1.03x faster                                               |
| xml_etree_generate         | 85.7 ms                                                          | 83.4 ms: 1.03x faster                                               |
| asyncio_tcp                | 378 ms                                                           | 370 ms: 1.02x faster                                                |
| async_tree_io              | 873 ms                                                           | 856 ms: 1.02x faster                                                |
| json_dumps                 | 10.8 ms                                                          | 10.6 ms: 1.02x faster                                               |
| generators                 | 33.5 ms                                                          | 33.4 ms: 1.00x faster                                               |
| pickle_dict                | 32.8 us                                                          | 32.7 us: 1.00x faster                                               |
| regex_v8                   | 26.0 ms                                                          | 26.0 ms: 1.00x faster                                               |
| pickle_pure_python         | 307 us                                                           | 309 us: 1.01x slower                                                |
| sqlglot_parse              | 1.39 ms                                                          | 1.40 ms: 1.01x slower                                               |
| xml_etree_iterparse        | 103 ms                                                           | 103 ms: 1.01x slower                                                |
| chameleon                  | 7.40 ms                                                          | 7.46 ms: 1.01x slower                                               |
| pickle                     | 10.6 us                                                          | 10.7 us: 1.01x slower                                               |
| pyflate                    | 482 ms                                                           | 487 ms: 1.01x slower                                                |
| deepcopy_reduce            | 3.39 us                                                          | 3.43 us: 1.01x slower                                               |
| logging_silent             | 96.3 ns                                                          | 97.8 ns: 1.02x slower                                               |
| pycparser                  | 1.22 sec                                                         | 1.24 sec: 1.02x slower                                              |
| logging_simple             | 6.40 us                                                          | 6.52 us: 1.02x slower                                               |
| genshi_text                | 25.9 ms                                                          | 26.4 ms: 1.02x slower                                               |
| tornado_http               | 119 ms                                                           | 122 ms: 1.02x slower                                                |
| xml_etree_parse            | 144 ms                                                           | 146 ms: 1.02x slower                                                |
| json_loads                 | 25.0 us                                                          | 25.5 us: 1.02x slower                                               |
| sqlglot_normalize          | 120 ms                                                           | 123 ms: 1.02x slower                                                |
| json                       | 5.35 ms                                                          | 5.47 ms: 1.02x slower                                               |
| dulwich_log                | 67.3 ms                                                          | 68.7 ms: 1.02x slower                                               |
| python_startup             | 13.2 ms                                                          | 13.5 ms: 1.02x slower                                               |
| pprint_safe_repr           | 818 ms                                                           | 836 ms: 1.02x slower                                                |
| 2to3                       | 291 ms                                                           | 298 ms: 1.02x slower                                                |
| sympy_expand               | 501 ms                                                           | 513 ms: 1.02x slower                                                |
| thrift                     | 880 us                                                           | 902 us: 1.03x slower                                                |
| sqlglot_transpile          | 1.76 ms                                                          | 1.81 ms: 1.03x slower                                               |
| regex_compile              | 144 ms                                                           | 148 ms: 1.03x slower                                                |
| pidigits                   | 254 ms                                                           | 261 ms: 1.03x slower                                                |
| deepcopy_memo              | 37.3 us                                                          | 38.4 us: 1.03x slower                                               |
| dask                       | 391 ms                                                           | 403 ms: 1.03x slower                                                |
| pprint_pformat             | 1.66 sec                                                         | 1.71 sec: 1.03x slower                                              |
| deepcopy                   | 377 us                                                           | 390 us: 1.03x slower                                                |
| async_tree_cpu_io_mixed_tg | 573 ms                                                           | 592 ms: 1.03x slower                                                |
| meteor_contest             | 128 ms                                                           | 133 ms: 1.03x slower                                                |
| regex_effbot               | 3.40 ms                                                          | 3.52 ms: 1.03x slower                                               |
| coverage                   | 83.5 ms                                                          | 86.4 ms: 1.03x slower                                               |
| sympy_str                  | 295 ms                                                           | 305 ms: 1.04x slower                                                |
| async_tree_none            | 365 ms                                                           | 379 ms: 1.04x slower                                                |
| docutils                   | 2.98 sec                                                         | 3.10 sec: 1.04x slower                                              |
| unpickle_pure_python       | 224 us                                                           | 234 us: 1.04x slower                                                |
| crypto_pyaes               | 73.6 ms                                                          | 76.7 ms: 1.04x slower                                               |
| aiohttp                    | 1.07 ms                                                          | 1.13 ms: 1.05x slower                                               |
| sqlglot_optimize           | 59.5 ms                                                          | 62.7 ms: 1.05x slower                                               |
| mdp                        | 2.46 sec                                                         | 2.59 sec: 1.05x slower                                              |
| gunicorn                   | 1.04 ms                                                          | 1.10 ms: 1.05x slower                                               |
| go                         | 165 ms                                                           | 175 ms: 1.06x slower                                                |
| scimark_monte_carlo        | 65.5 ms                                                          | 69.5 ms: 1.06x slower                                               |
| sympy_sum                  | 155 ms                                                           | 164 ms: 1.06x slower                                                |
| coroutines                 | 22.0 ms                                                          | 23.4 ms: 1.07x slower                                               |
| deltablue                  | 3.37 ms                                                          | 3.61 ms: 1.07x slower                                               |
| chaos                      | 59.6 ms                                                          | 63.8 ms: 1.07x slower                                               |
| mypy2                      | 764 ms                                                           | 827 ms: 1.08x slower                                                |
| nbody                      | 87.8 ms                                                          | 95.1 ms: 1.08x slower                                               |
| fannkuch                   | 353 ms                                                           | 384 ms: 1.09x slower                                                |
| async_generators           | 363 ms                                                           | 397 ms: 1.09x slower                                                |
| sympy_integrate            | 23.2 ms                                                          | 25.4 ms: 1.10x slower                                               |
| raytrace                   | 260 ms                                                           | 291 ms: 1.12x slower                                                |
| pathlib                    | 17.1 ms                                                          | 19.5 ms: 1.14x slower                                               |
| comprehensions             | 17.0 us                                                          | 19.5 us: 1.15x slower                                               |
| nqueens                    | 88.4 ms                                                          | 103 ms: 1.16x slower                                                |
| hexiom                     | 6.35 ms                                                          | 7.39 ms: 1.16x slower                                               |
| bench_thread_pool          | 908 us                                                           | 1.10 ms: 1.21x slower                                               |
| scimark_lu                 | 97.5 ms                                                          | 124 ms: 1.27x slower                                                |
| scimark_sor                | 119 ms                                                           | 153 ms: 1.29x slower                                                |
| python_startup_no_site     | 8.85 ms                                                          | 11.8 ms: 1.33x slower                                               |
| Geometric mean             | (ref)                                                            | 1.02x slower                                                        |

Benchmark hidden because not significant (12): async_tree_memoization, async_tree_none_tg, asyncio_websockets, pickle_list, pylint, genshi_xml, asyncio_tcp_ssl, scimark_fft, logging_format, async_tree_cpu_io_mixed, async_tree_memoization_tg, bench_mp_pool
Ignored benchmarks (3) of results/bm-20240605-3.13.0b2-3a83b17/bm-20240605-pythonperf2-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17.json: bpe_tokeniser, django_template, flaskblogging

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.01x
- 95% likely to have a slowdown of 1.01x
- 99% likely to have a slowdown of 1.01x

# Memory
- memory change: 1.06x