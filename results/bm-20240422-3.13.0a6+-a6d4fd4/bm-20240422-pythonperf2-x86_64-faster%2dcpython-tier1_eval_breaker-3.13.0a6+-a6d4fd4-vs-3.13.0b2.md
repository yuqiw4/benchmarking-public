# Results vs. 3.13.0b2

- fork: faster-cpython
- ref: tier1_eval_breaker
- machine: linux-x86_64
- commit hash: a6d4fd4
- commit date: 2024-04-22
- overall geometric mean: 1.01x faster
- HPT reliability: 89.02%
- HPT 99th percentile: 1.00x faster
- Memory change: 0.99x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240605-pythonperf2-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240422-pythonperf2-x86_64-faster%2dcpython-tier1_eval_breaker-3.13.0a6+-a6d4fd4 |
|----------------|:----------------------------------------------------------------:|:------------------------------------------------------------------------------------:|
| 2to3           | 291 ms                                                           | 287 ms: 1.02x faster                                                                 |
| chameleon      | 7.40 ms                                                          | 7.29 ms: 1.01x faster                                                                |
| html5lib       | 74.7 ms                                                          | 72.6 ms: 1.03x faster                                                                |
| Geometric mean | (ref)                                                            | 1.01x faster                                                                         |

Benchmark hidden because not significant (2): docutils, tornado_http

Benchmarks with tag 'asyncio':
==============================

| Benchmark      | bm-20240605-pythonperf2-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240422-pythonperf2-x86_64-faster%2dcpython-tier1_eval_breaker-3.13.0a6+-a6d4fd4 |
|----------------|:----------------------------------------------------------------:|:------------------------------------------------------------------------------------:|
| async_tree_io  | 873 ms                                                           | 900 ms: 1.03x slower                                                                 |
| Geometric mean | (ref)                                                            | 1.00x slower                                                                         |

Benchmark hidden because not significant (7): async_tree_io_tg, async_tree_none_tg, async_tree_memoization_tg, async_tree_cpu_io_mixed_tg, async_tree_none, async_tree_memoization, async_tree_cpu_io_mixed

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240605-pythonperf2-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240422-pythonperf2-x86_64-faster%2dcpython-tier1_eval_breaker-3.13.0a6+-a6d4fd4 |
|----------------|:----------------------------------------------------------------:|:------------------------------------------------------------------------------------:|
| float          | 80.2 ms                                                          | 77.2 ms: 1.04x faster                                                                |
| pidigits       | 254 ms                                                           | 262 ms: 1.03x slower                                                                 |
| Geometric mean | (ref)                                                            | 1.01x faster                                                                         |

Benchmark hidden because not significant (1): nbody

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240605-pythonperf2-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240422-pythonperf2-x86_64-faster%2dcpython-tier1_eval_breaker-3.13.0a6+-a6d4fd4 |
|----------------|:----------------------------------------------------------------:|:------------------------------------------------------------------------------------:|
| regex_dna      | 249 ms                                                           | 238 ms: 1.05x faster                                                                 |
| regex_compile  | 144 ms                                                           | 143 ms: 1.01x faster                                                                 |
| regex_v8       | 26.0 ms                                                          | 26.0 ms: 1.00x faster                                                                |
| regex_effbot   | 3.40 ms                                                          | 3.47 ms: 1.02x slower                                                                |
| Geometric mean | (ref)                                                            | 1.01x faster                                                                         |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240605-pythonperf2-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240422-pythonperf2-x86_64-faster%2dcpython-tier1_eval_breaker-3.13.0a6+-a6d4fd4 |
|----------------------|:----------------------------------------------------------------:|:------------------------------------------------------------------------------------:|
| tomli_loads          | 2.40 sec                                                         | 2.18 sec: 1.10x faster                                                               |
| unpickle_pure_python | 224 us                                                           | 204 us: 1.10x faster                                                                 |
| unpickle             | 15.7 us                                                          | 14.8 us: 1.06x faster                                                                |
| unpickle_list        | 4.70 us                                                          | 4.56 us: 1.03x faster                                                                |
| json_dumps           | 10.8 ms                                                          | 10.6 ms: 1.02x faster                                                                |
| pickle               | 10.6 us                                                          | 10.5 us: 1.01x faster                                                                |
| json_loads           | 25.0 us                                                          | 24.8 us: 1.01x faster                                                                |
| xml_etree_generate   | 85.7 ms                                                          | 85.1 ms: 1.01x faster                                                                |
| pickle_pure_python   | 307 us                                                           | 310 us: 1.01x slower                                                                 |
| xml_etree_iterparse  | 103 ms                                                           | 104 ms: 1.01x slower                                                                 |
| pickle_dict          | 32.8 us                                                          | 33.3 us: 1.02x slower                                                                |
| xml_etree_parse      | 144 ms                                                           | 146 ms: 1.02x slower                                                                 |
| Geometric mean       | (ref)                                                            | 1.02x faster                                                                         |

Benchmark hidden because not significant (2): xml_etree_process, pickle_list

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240605-pythonperf2-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240422-pythonperf2-x86_64-faster%2dcpython-tier1_eval_breaker-3.13.0a6+-a6d4fd4 |
|------------------------|:----------------------------------------------------------------:|:------------------------------------------------------------------------------------:|
| python_startup         | 13.2 ms                                                          | 12.9 ms: 1.03x faster                                                                |
| python_startup_no_site | 8.85 ms                                                          | 8.84 ms: 1.00x faster                                                                |
| Geometric mean         | (ref)                                                            | 1.01x faster                                                                         |

Benchmarks with tag 'template':
===============================

| Benchmark      | bm-20240605-pythonperf2-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240422-pythonperf2-x86_64-faster%2dcpython-tier1_eval_breaker-3.13.0a6+-a6d4fd4 |
|----------------|:----------------------------------------------------------------:|:------------------------------------------------------------------------------------:|
| genshi_xml     | 58.1 ms                                                          | 56.2 ms: 1.03x faster                                                                |
| mako           | 10.4 ms                                                          | 10.5 ms: 1.01x slower                                                                |
| genshi_text    | 25.9 ms                                                          | 26.4 ms: 1.02x slower                                                                |
| Geometric mean | (ref)                                                            | 1.00x faster                                                                         |

Benchmark hidden because not significant (1): django_template

All benchmarks:
===============

| Benchmark                | bm-20240605-pythonperf2-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240422-pythonperf2-x86_64-faster%2dcpython-tier1_eval_breaker-3.13.0a6+-a6d4fd4 |
|--------------------------|:----------------------------------------------------------------:|:------------------------------------------------------------------------------------:|
| typing_runtime_protocols | 171 us                                                           | 118 us: 1.45x faster                                                                 |
| tomli_loads              | 2.40 sec                                                         | 2.18 sec: 1.10x faster                                                               |
| unpickle_pure_python     | 224 us                                                           | 204 us: 1.10x faster                                                                 |
| bench_mp_pool            | 4.91 ms                                                          | 4.50 ms: 1.09x faster                                                                |
| go                       | 165 ms                                                           | 155 ms: 1.07x faster                                                                 |
| unpickle                 | 15.7 us                                                          | 14.8 us: 1.06x faster                                                                |
| gc_traversal             | 4.69 ms                                                          | 4.42 ms: 1.06x faster                                                                |
| richards_super           | 61.2 ms                                                          | 58.0 ms: 1.05x faster                                                                |
| regex_dna                | 249 ms                                                           | 238 ms: 1.05x faster                                                                 |
| scimark_fft              | 312 ms                                                           | 298 ms: 1.05x faster                                                                 |
| telco                    | 8.40 ms                                                          | 8.06 ms: 1.04x faster                                                                |
| hexiom                   | 6.35 ms                                                          | 6.10 ms: 1.04x faster                                                                |
| create_gc_cycles         | 2.00 ms                                                          | 1.93 ms: 1.04x faster                                                                |
| coroutines               | 22.0 ms                                                          | 21.2 ms: 1.04x faster                                                                |
| float                    | 80.2 ms                                                          | 77.2 ms: 1.04x faster                                                                |
| scimark_monte_carlo      | 65.5 ms                                                          | 63.2 ms: 1.04x faster                                                                |
| richards                 | 53.4 ms                                                          | 51.5 ms: 1.04x faster                                                                |
| genshi_xml               | 58.1 ms                                                          | 56.2 ms: 1.03x faster                                                                |
| logging_format           | 7.11 us                                                          | 6.91 us: 1.03x faster                                                                |
| pyflate                  | 482 ms                                                           | 468 ms: 1.03x faster                                                                 |
| unpickle_list            | 4.70 us                                                          | 4.56 us: 1.03x faster                                                                |
| html5lib                 | 74.7 ms                                                          | 72.6 ms: 1.03x faster                                                                |
| raytrace                 | 260 ms                                                           | 253 ms: 1.03x faster                                                                 |
| bench_thread_pool        | 908 us                                                           | 884 us: 1.03x faster                                                                 |
| python_startup           | 13.2 ms                                                          | 12.9 ms: 1.03x faster                                                                |
| sqlglot_normalize        | 120 ms                                                           | 117 ms: 1.02x faster                                                                 |
| nqueens                  | 88.4 ms                                                          | 86.6 ms: 1.02x faster                                                                |
| pprint_safe_repr         | 818 ms                                                           | 801 ms: 1.02x faster                                                                 |
| async_generators         | 363 ms                                                           | 356 ms: 1.02x faster                                                                 |
| logging_silent           | 96.3 ns                                                          | 94.6 ns: 1.02x faster                                                                |
| chaos                    | 59.6 ms                                                          | 58.6 ms: 1.02x faster                                                                |
| 2to3                     | 291 ms                                                           | 287 ms: 1.02x faster                                                                 |
| deltablue                | 3.37 ms                                                          | 3.32 ms: 1.02x faster                                                                |
| json_dumps               | 10.8 ms                                                          | 10.6 ms: 1.02x faster                                                                |
| chameleon                | 7.40 ms                                                          | 7.29 ms: 1.01x faster                                                                |
| pprint_pformat           | 1.66 sec                                                         | 1.64 sec: 1.01x faster                                                               |
| asyncio_tcp              | 378 ms                                                           | 373 ms: 1.01x faster                                                                 |
| crypto_pyaes             | 73.6 ms                                                          | 72.6 ms: 1.01x faster                                                                |
| generators               | 33.5 ms                                                          | 33.1 ms: 1.01x faster                                                                |
| logging_simple           | 6.40 us                                                          | 6.32 us: 1.01x faster                                                                |
| pickle                   | 10.6 us                                                          | 10.5 us: 1.01x faster                                                                |
| sqlite_synth             | 2.80 us                                                          | 2.77 us: 1.01x faster                                                                |
| json_loads               | 25.0 us                                                          | 24.8 us: 1.01x faster                                                                |
| sqlglot_optimize         | 59.5 ms                                                          | 59.0 ms: 1.01x faster                                                                |
| regex_compile            | 144 ms                                                           | 143 ms: 1.01x faster                                                                 |
| xml_etree_generate       | 85.7 ms                                                          | 85.1 ms: 1.01x faster                                                                |
| spectral_norm            | 97.3 ms                                                          | 96.6 ms: 1.01x faster                                                                |
| comprehensions           | 17.0 us                                                          | 16.8 us: 1.01x faster                                                                |
| meteor_contest           | 128 ms                                                           | 127 ms: 1.01x faster                                                                 |
| sympy_sum                | 155 ms                                                           | 154 ms: 1.00x faster                                                                 |
| sympy_integrate          | 23.2 ms                                                          | 23.1 ms: 1.00x faster                                                                |
| regex_v8                 | 26.0 ms                                                          | 26.0 ms: 1.00x faster                                                                |
| python_startup_no_site   | 8.85 ms                                                          | 8.84 ms: 1.00x faster                                                                |
| dulwich_log              | 67.3 ms                                                          | 67.7 ms: 1.01x slower                                                                |
| sympy_expand             | 501 ms                                                           | 504 ms: 1.01x slower                                                                 |
| pickle_pure_python       | 307 us                                                           | 310 us: 1.01x slower                                                                 |
| scimark_sparse_mat_mult  | 4.28 ms                                                          | 4.32 ms: 1.01x slower                                                                |
| deepcopy_reduce          | 3.39 us                                                          | 3.42 us: 1.01x slower                                                                |
| mako                     | 10.4 ms                                                          | 10.5 ms: 1.01x slower                                                                |
| xml_etree_iterparse      | 103 ms                                                           | 104 ms: 1.01x slower                                                                 |
| sympy_str                | 295 ms                                                           | 298 ms: 1.01x slower                                                                 |
| scimark_lu               | 97.5 ms                                                          | 98.6 ms: 1.01x slower                                                                |
| sqlglot_transpile        | 1.76 ms                                                          | 1.79 ms: 1.01x slower                                                                |
| sqlglot_parse            | 1.39 ms                                                          | 1.41 ms: 1.01x slower                                                                |
| pickle_dict              | 32.8 us                                                          | 33.3 us: 1.02x slower                                                                |
| xml_etree_parse          | 144 ms                                                           | 146 ms: 1.02x slower                                                                 |
| mdp                      | 2.46 sec                                                         | 2.50 sec: 1.02x slower                                                               |
| deepcopy_memo            | 37.3 us                                                          | 37.9 us: 1.02x slower                                                                |
| genshi_text              | 25.9 ms                                                          | 26.4 ms: 1.02x slower                                                                |
| json                     | 5.35 ms                                                          | 5.46 ms: 1.02x slower                                                                |
| regex_effbot             | 3.40 ms                                                          | 3.47 ms: 1.02x slower                                                                |
| fannkuch                 | 353 ms                                                           | 361 ms: 1.02x slower                                                                 |
| thrift                   | 880 us                                                           | 900 us: 1.02x slower                                                                 |
| async_tree_io            | 873 ms                                                           | 900 ms: 1.03x slower                                                                 |
| pidigits                 | 254 ms                                                           | 262 ms: 1.03x slower                                                                 |
| coverage                 | 83.5 ms                                                          | 86.3 ms: 1.03x slower                                                                |
| pycparser                | 1.22 sec                                                         | 1.28 sec: 1.05x slower                                                               |
| Geometric mean           | (ref)                                                            | 1.01x faster                                                                         |

Benchmark hidden because not significant (23): async_tree_io_tg, nbody, async_tree_none_tg, async_tree_memoization_tg, django_template, xml_etree_process, pickle_list, asyncio_tcp_ssl, aiohttp, pathlib, dask, docutils, gunicorn, scimark_sor, deepcopy, asyncio_websockets, async_tree_cpu_io_mixed_tg, tornado_http, async_tree_none, async_tree_memoization, mypy2, async_tree_cpu_io_mixed, pylint
Ignored benchmarks (2) of results/bm-20240605-3.13.0b2-3a83b17/bm-20240605-pythonperf2-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17.json: bpe_tokeniser, flaskblogging

# HPT report

- Reliability score: 89.02% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 0.99x