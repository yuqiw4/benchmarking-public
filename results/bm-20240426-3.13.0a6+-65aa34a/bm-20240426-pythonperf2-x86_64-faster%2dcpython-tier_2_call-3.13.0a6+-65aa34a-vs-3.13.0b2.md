# Results vs. 3.13.0b2

- fork: faster-cpython
- ref: tier_2_call
- machine: linux-x86_64
- commit hash: 65aa34a
- commit date: 2024-04-26
- overall geometric mean: 1.01x faster
- HPT reliability: 99.98%
- HPT 99th percentile: 1.00x faster
- Memory change: 0.98x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240605-pythonperf2-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240426-pythonperf2-x86_64-faster%2dcpython-tier_2_call-3.13.0a6+-65aa34a |
|----------------|:----------------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| 2to3           | 291 ms                                                           | 286 ms: 1.02x faster                                                          |
| chameleon      | 7.40 ms                                                          | 7.18 ms: 1.03x faster                                                         |
| docutils       | 2.98 sec                                                         | 3.00 sec: 1.01x slower                                                        |
| html5lib       | 74.7 ms                                                          | 73.0 ms: 1.02x faster                                                         |
| Geometric mean | (ref)                                                            | 1.01x faster                                                                  |

Benchmark hidden because not significant (1): tornado_http

Benchmarks with tag 'asyncio':
==============================

| Benchmark          | bm-20240605-pythonperf2-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240426-pythonperf2-x86_64-faster%2dcpython-tier_2_call-3.13.0a6+-65aa34a |
|--------------------|:----------------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| async_tree_none_tg | 340 ms                                                           | 329 ms: 1.04x faster                                                          |
| async_tree_io_tg   | 900 ms                                                           | 888 ms: 1.01x faster                                                          |
| Geometric mean     | (ref)                                                            | 1.01x faster                                                                  |

Benchmark hidden because not significant (6): async_tree_io, async_tree_memoization_tg, async_tree_none, async_tree_memoization, async_tree_cpu_io_mixed_tg, async_tree_cpu_io_mixed

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240605-pythonperf2-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240426-pythonperf2-x86_64-faster%2dcpython-tier_2_call-3.13.0a6+-65aa34a |
|----------------|:----------------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| float          | 80.2 ms                                                          | 77.4 ms: 1.04x faster                                                         |
| nbody          | 87.8 ms                                                          | 86.5 ms: 1.01x faster                                                         |
| pidigits       | 254 ms                                                           | 262 ms: 1.03x slower                                                          |
| Geometric mean | (ref)                                                            | 1.01x faster                                                                  |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240605-pythonperf2-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240426-pythonperf2-x86_64-faster%2dcpython-tier_2_call-3.13.0a6+-65aa34a |
|----------------|:----------------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| regex_dna      | 249 ms                                                           | 239 ms: 1.04x faster                                                          |
| regex_compile  | 144 ms                                                           | 142 ms: 1.02x faster                                                          |
| regex_effbot   | 3.40 ms                                                          | 3.70 ms: 1.09x slower                                                         |
| Geometric mean | (ref)                                                            | 1.01x slower                                                                  |

Benchmark hidden because not significant (1): regex_v8

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240605-pythonperf2-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240426-pythonperf2-x86_64-faster%2dcpython-tier_2_call-3.13.0a6+-65aa34a |
|----------------------|:----------------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| tomli_loads          | 2.40 sec                                                         | 2.23 sec: 1.08x faster                                                        |
| unpickle_pure_python | 224 us                                                           | 212 us: 1.06x faster                                                          |
| unpickle             | 15.7 us                                                          | 15.3 us: 1.03x faster                                                         |
| unpickle_list        | 4.70 us                                                          | 4.58 us: 1.03x faster                                                         |
| pickle               | 10.6 us                                                          | 10.4 us: 1.02x faster                                                         |
| json_loads           | 25.0 us                                                          | 24.6 us: 1.02x faster                                                         |
| pickle_dict          | 32.8 us                                                          | 32.2 us: 1.02x faster                                                         |
| json_dumps           | 10.8 ms                                                          | 10.6 ms: 1.02x faster                                                         |
| xml_etree_process    | 59.7 ms                                                          | 59.0 ms: 1.01x faster                                                         |
| xml_etree_generate   | 85.7 ms                                                          | 84.8 ms: 1.01x faster                                                         |
| pickle_list          | 4.44 us                                                          | 4.52 us: 1.02x slower                                                         |
| xml_etree_iterparse  | 103 ms                                                           | 106 ms: 1.04x slower                                                          |
| xml_etree_parse      | 144 ms                                                           | 150 ms: 1.04x slower                                                          |
| Geometric mean       | (ref)                                                            | 1.01x faster                                                                  |

Benchmark hidden because not significant (1): pickle_pure_python

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240605-pythonperf2-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240426-pythonperf2-x86_64-faster%2dcpython-tier_2_call-3.13.0a6+-65aa34a |
|------------------------|:----------------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| python_startup         | 13.2 ms                                                          | 12.9 ms: 1.03x faster                                                         |
| python_startup_no_site | 8.85 ms                                                          | 8.81 ms: 1.01x faster                                                         |
| Geometric mean         | (ref)                                                            | 1.02x faster                                                                  |

Benchmarks with tag 'template':
===============================

| Benchmark      | bm-20240605-pythonperf2-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240426-pythonperf2-x86_64-faster%2dcpython-tier_2_call-3.13.0a6+-65aa34a |
|----------------|:----------------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| genshi_xml     | 58.1 ms                                                          | 54.0 ms: 1.08x faster                                                         |
| genshi_text    | 25.9 ms                                                          | 24.8 ms: 1.04x faster                                                         |
| mako           | 10.4 ms                                                          | 10.2 ms: 1.02x faster                                                         |
| Geometric mean | (ref)                                                            | 1.04x faster                                                                  |

Benchmark hidden because not significant (1): django_template

All benchmarks:
===============

| Benchmark                | bm-20240605-pythonperf2-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240426-pythonperf2-x86_64-faster%2dcpython-tier_2_call-3.13.0a6+-65aa34a |
|--------------------------|:----------------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| bench_mp_pool            | 4.91 ms                                                          | 4.35 ms: 1.13x faster                                                         |
| genshi_xml               | 58.1 ms                                                          | 54.0 ms: 1.08x faster                                                         |
| tomli_loads              | 2.40 sec                                                         | 2.23 sec: 1.08x faster                                                        |
| coroutines               | 22.0 ms                                                          | 20.6 ms: 1.07x faster                                                         |
| pyflate                  | 482 ms                                                           | 454 ms: 1.06x faster                                                          |
| hexiom                   | 6.35 ms                                                          | 5.99 ms: 1.06x faster                                                         |
| scimark_monte_carlo      | 65.5 ms                                                          | 61.8 ms: 1.06x faster                                                         |
| gc_traversal             | 4.69 ms                                                          | 4.42 ms: 1.06x faster                                                         |
| unpickle_pure_python     | 224 us                                                           | 212 us: 1.06x faster                                                          |
| telco                    | 8.40 ms                                                          | 7.97 ms: 1.05x faster                                                         |
| deltablue                | 3.37 ms                                                          | 3.22 ms: 1.05x faster                                                         |
| richards_super           | 61.2 ms                                                          | 58.4 ms: 1.05x faster                                                         |
| genshi_text              | 25.9 ms                                                          | 24.8 ms: 1.04x faster                                                         |
| regex_dna                | 249 ms                                                           | 239 ms: 1.04x faster                                                          |
| scimark_fft              | 312 ms                                                           | 301 ms: 1.04x faster                                                          |
| async_tree_none_tg       | 340 ms                                                           | 329 ms: 1.04x faster                                                          |
| float                    | 80.2 ms                                                          | 77.4 ms: 1.04x faster                                                         |
| go                       | 165 ms                                                           | 160 ms: 1.03x faster                                                          |
| crypto_pyaes             | 73.6 ms                                                          | 71.3 ms: 1.03x faster                                                         |
| chameleon                | 7.40 ms                                                          | 7.18 ms: 1.03x faster                                                         |
| asyncio_tcp              | 378 ms                                                           | 367 ms: 1.03x faster                                                          |
| richards                 | 53.4 ms                                                          | 52.0 ms: 1.03x faster                                                         |
| python_startup           | 13.2 ms                                                          | 12.9 ms: 1.03x faster                                                         |
| unpickle                 | 15.7 us                                                          | 15.3 us: 1.03x faster                                                         |
| create_gc_cycles         | 2.00 ms                                                          | 1.95 ms: 1.03x faster                                                         |
| unpickle_list            | 4.70 us                                                          | 4.58 us: 1.03x faster                                                         |
| logging_silent           | 96.3 ns                                                          | 93.9 ns: 1.02x faster                                                         |
| pprint_safe_repr         | 818 ms                                                           | 798 ms: 1.02x faster                                                          |
| html5lib                 | 74.7 ms                                                          | 73.0 ms: 1.02x faster                                                         |
| sqlglot_normalize        | 120 ms                                                           | 118 ms: 1.02x faster                                                          |
| mako                     | 10.4 ms                                                          | 10.2 ms: 1.02x faster                                                         |
| scimark_lu               | 97.5 ms                                                          | 95.4 ms: 1.02x faster                                                         |
| sqlite_synth             | 2.80 us                                                          | 2.74 us: 1.02x faster                                                         |
| pickle                   | 10.6 us                                                          | 10.4 us: 1.02x faster                                                         |
| bench_thread_pool        | 908 us                                                           | 890 us: 1.02x faster                                                          |
| 2to3                     | 291 ms                                                           | 286 ms: 1.02x faster                                                          |
| json_loads               | 25.0 us                                                          | 24.6 us: 1.02x faster                                                         |
| pickle_dict              | 32.8 us                                                          | 32.2 us: 1.02x faster                                                         |
| pprint_pformat           | 1.66 sec                                                         | 1.63 sec: 1.02x faster                                                        |
| json_dumps               | 10.8 ms                                                          | 10.6 ms: 1.02x faster                                                         |
| regex_compile            | 144 ms                                                           | 142 ms: 1.02x faster                                                          |
| nbody                    | 87.8 ms                                                          | 86.5 ms: 1.01x faster                                                         |
| dulwich_log              | 67.3 ms                                                          | 66.4 ms: 1.01x faster                                                         |
| async_tree_io_tg         | 900 ms                                                           | 888 ms: 1.01x faster                                                          |
| raytrace                 | 260 ms                                                           | 257 ms: 1.01x faster                                                          |
| chaos                    | 59.6 ms                                                          | 58.8 ms: 1.01x faster                                                         |
| xml_etree_process        | 59.7 ms                                                          | 59.0 ms: 1.01x faster                                                         |
| logging_format           | 7.11 us                                                          | 7.03 us: 1.01x faster                                                         |
| xml_etree_generate       | 85.7 ms                                                          | 84.8 ms: 1.01x faster                                                         |
| sqlglot_optimize         | 59.5 ms                                                          | 58.9 ms: 1.01x faster                                                         |
| asyncio_websockets       | 395 ms                                                           | 391 ms: 1.01x faster                                                          |
| sympy_sum                | 155 ms                                                           | 153 ms: 1.01x faster                                                          |
| nqueens                  | 88.4 ms                                                          | 87.6 ms: 1.01x faster                                                         |
| sqlglot_parse            | 1.39 ms                                                          | 1.38 ms: 1.01x faster                                                         |
| python_startup_no_site   | 8.85 ms                                                          | 8.81 ms: 1.01x faster                                                         |
| generators               | 33.5 ms                                                          | 33.4 ms: 1.00x faster                                                         |
| asyncio_tcp_ssl          | 1.58 sec                                                         | 1.57 sec: 1.00x faster                                                        |
| sympy_expand             | 501 ms                                                           | 499 ms: 1.00x faster                                                          |
| meteor_contest           | 128 ms                                                           | 128 ms: 1.00x faster                                                          |
| sympy_str                | 295 ms                                                           | 294 ms: 1.00x faster                                                          |
| sympy_integrate          | 23.2 ms                                                          | 23.3 ms: 1.00x slower                                                         |
| pathlib                  | 17.1 ms                                                          | 17.2 ms: 1.00x slower                                                         |
| comprehensions           | 17.0 us                                                          | 17.1 us: 1.01x slower                                                         |
| docutils                 | 2.98 sec                                                         | 3.00 sec: 1.01x slower                                                        |
| async_generators         | 363 ms                                                           | 365 ms: 1.01x slower                                                          |
| fannkuch                 | 353 ms                                                           | 356 ms: 1.01x slower                                                          |
| typing_runtime_protocols | 171 us                                                           | 173 us: 1.01x slower                                                          |
| mdp                      | 2.46 sec                                                         | 2.50 sec: 1.02x slower                                                        |
| pickle_list              | 4.44 us                                                          | 4.52 us: 1.02x slower                                                         |
| scimark_sparse_mat_mult  | 4.28 ms                                                          | 4.36 ms: 1.02x slower                                                         |
| coverage                 | 83.5 ms                                                          | 85.3 ms: 1.02x slower                                                         |
| deepcopy                 | 377 us                                                           | 386 us: 1.02x slower                                                          |
| pycparser                | 1.22 sec                                                         | 1.26 sec: 1.03x slower                                                        |
| pidigits                 | 254 ms                                                           | 262 ms: 1.03x slower                                                          |
| xml_etree_iterparse      | 103 ms                                                           | 106 ms: 1.04x slower                                                          |
| scimark_sor              | 119 ms                                                           | 123 ms: 1.04x slower                                                          |
| deepcopy_memo            | 37.3 us                                                          | 38.9 us: 1.04x slower                                                         |
| xml_etree_parse          | 144 ms                                                           | 150 ms: 1.04x slower                                                          |
| deepcopy_reduce          | 3.39 us                                                          | 3.56 us: 1.05x slower                                                         |
| regex_effbot             | 3.40 ms                                                          | 3.70 ms: 1.09x slower                                                         |
| Geometric mean           | (ref)                                                            | 1.01x faster                                                                  |

Benchmark hidden because not significant (20): async_tree_io, async_tree_memoization_tg, django_template, async_tree_none, aiohttp, async_tree_memoization, thrift, tornado_http, dask, pickle_pure_python, async_tree_cpu_io_mixed_tg, logging_simple, async_tree_cpu_io_mixed, sqlglot_transpile, json, spectral_norm, mypy2, gunicorn, regex_v8, pylint
Ignored benchmarks (2) of results/bm-20240605-3.13.0b2-3a83b17/bm-20240605-pythonperf2-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17.json: bpe_tokeniser, flaskblogging

# HPT report

- Reliability score: 99.98% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 0.98x