# Results vs. 3.13.0b2

- fork: python
- ref: main
- machine: linux-x86_64
- commit hash: c32dc47
- commit date: 2024-04-02
- overall geometric mean: 1.01x faster
- HPT reliability: 99.97%
- HPT 99th percentile: 1.00x faster
- Memory change: 0.97x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240605-pythonperf2-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240402-pythonperf2-x86_64-python-main-3.13.0a5+-c32dc47 |
|----------------|:----------------------------------------------------------------:|:------------------------------------------------------------:|
| 2to3           | 291 ms                                                           | 288 ms: 1.01x faster                                         |
| chameleon      | 7.40 ms                                                          | 7.15 ms: 1.03x faster                                        |
| docutils       | 2.98 sec                                                         | 2.97 sec: 1.00x faster                                       |
| html5lib       | 74.7 ms                                                          | 73.2 ms: 1.02x faster                                        |
| Geometric mean | (ref)                                                            | 1.01x faster                                                 |

Benchmark hidden because not significant (1): tornado_http

Benchmarks with tag 'asyncio':
==============================

| Benchmark        | bm-20240605-pythonperf2-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240402-pythonperf2-x86_64-python-main-3.13.0a5+-c32dc47 |
|------------------|:----------------------------------------------------------------:|:------------------------------------------------------------:|
| async_tree_io_tg | 900 ms                                                           | 854 ms: 1.05x faster                                         |
| Geometric mean   | (ref)                                                            | 1.01x faster                                                 |

Benchmark hidden because not significant (7): async_tree_none_tg, async_tree_memoization_tg, async_tree_none, async_tree_memoization, async_tree_cpu_io_mixed_tg, async_tree_cpu_io_mixed, async_tree_io

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240605-pythonperf2-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240402-pythonperf2-x86_64-python-main-3.13.0a5+-c32dc47 |
|----------------|:----------------------------------------------------------------:|:------------------------------------------------------------:|
| float          | 80.2 ms                                                          | 75.3 ms: 1.06x faster                                        |
| nbody          | 87.8 ms                                                          | 85.3 ms: 1.03x faster                                        |
| pidigits       | 254 ms                                                           | 263 ms: 1.04x slower                                         |
| Geometric mean | (ref)                                                            | 1.02x faster                                                 |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240605-pythonperf2-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240402-pythonperf2-x86_64-python-main-3.13.0a5+-c32dc47 |
|----------------|:----------------------------------------------------------------:|:------------------------------------------------------------:|
| regex_dna      | 249 ms                                                           | 230 ms: 1.08x faster                                         |
| regex_compile  | 144 ms                                                           | 141 ms: 1.02x faster                                         |
| regex_v8       | 26.0 ms                                                          | 25.7 ms: 1.01x faster                                        |
| regex_effbot   | 3.40 ms                                                          | 3.56 ms: 1.05x slower                                        |
| Geometric mean | (ref)                                                            | 1.02x faster                                                 |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240605-pythonperf2-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240402-pythonperf2-x86_64-python-main-3.13.0a5+-c32dc47 |
|----------------------|:----------------------------------------------------------------:|:------------------------------------------------------------:|
| tomli_loads          | 2.40 sec                                                         | 2.19 sec: 1.10x faster                                       |
| unpickle_pure_python | 224 us                                                           | 210 us: 1.07x faster                                         |
| unpickle             | 15.7 us                                                          | 14.9 us: 1.05x faster                                        |
| xml_etree_generate   | 85.7 ms                                                          | 82.4 ms: 1.04x faster                                        |
| xml_etree_process    | 59.7 ms                                                          | 57.5 ms: 1.04x faster                                        |
| json_dumps           | 10.8 ms                                                          | 10.5 ms: 1.03x faster                                        |
| unpickle_list        | 4.70 us                                                          | 4.62 us: 1.02x faster                                        |
| xml_etree_parse      | 144 ms                                                           | 142 ms: 1.01x faster                                         |
| pickle_pure_python   | 307 us                                                           | 305 us: 1.01x faster                                         |
| pickle               | 10.6 us                                                          | 10.5 us: 1.01x faster                                        |
| pickle_dict          | 32.8 us                                                          | 33.1 us: 1.01x slower                                        |
| xml_etree_iterparse  | 103 ms                                                           | 104 ms: 1.01x slower                                         |
| pickle_list          | 4.44 us                                                          | 4.53 us: 1.02x slower                                        |
| json_loads           | 25.0 us                                                          | 25.6 us: 1.02x slower                                        |
| Geometric mean       | (ref)                                                            | 1.02x faster                                                 |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240605-pythonperf2-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240402-pythonperf2-x86_64-python-main-3.13.0a5+-c32dc47 |
|------------------------|:----------------------------------------------------------------:|:------------------------------------------------------------:|
| python_startup         | 13.2 ms                                                          | 12.9 ms: 1.02x faster                                        |
| python_startup_no_site | 8.85 ms                                                          | 11.1 ms: 1.26x slower                                        |
| Geometric mean         | (ref)                                                            | 1.11x slower                                                 |

Benchmarks with tag 'template':
===============================

| Benchmark      | bm-20240605-pythonperf2-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240402-pythonperf2-x86_64-python-main-3.13.0a5+-c32dc47 |
|----------------|:----------------------------------------------------------------:|:------------------------------------------------------------:|
| genshi_xml     | 58.1 ms                                                          | 53.1 ms: 1.09x faster                                        |
| genshi_text    | 25.9 ms                                                          | 25.1 ms: 1.03x faster                                        |
| mako           | 10.4 ms                                                          | 10.3 ms: 1.01x faster                                        |
| Geometric mean | (ref)                                                            | 1.04x faster                                                 |

All benchmarks:
===============

| Benchmark                | bm-20240605-pythonperf2-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240402-pythonperf2-x86_64-python-main-3.13.0a5+-c32dc47 |
|--------------------------|:----------------------------------------------------------------:|:------------------------------------------------------------:|
| typing_runtime_protocols | 171 us                                                           | 114 us: 1.49x faster                                         |
| bench_mp_pool            | 4.91 ms                                                          | 4.47 ms: 1.10x faster                                        |
| tomli_loads              | 2.40 sec                                                         | 2.19 sec: 1.10x faster                                       |
| genshi_xml               | 58.1 ms                                                          | 53.1 ms: 1.09x faster                                        |
| regex_dna                | 249 ms                                                           | 230 ms: 1.08x faster                                         |
| richards_super           | 61.2 ms                                                          | 57.0 ms: 1.07x faster                                        |
| pylint                   | 339 ms                                                           | 317 ms: 1.07x faster                                         |
| unpickle_pure_python     | 224 us                                                           | 210 us: 1.07x faster                                         |
| richards                 | 53.4 ms                                                          | 50.1 ms: 1.07x faster                                        |
| float                    | 80.2 ms                                                          | 75.3 ms: 1.06x faster                                        |
| spectral_norm            | 97.3 ms                                                          | 92.3 ms: 1.05x faster                                        |
| unpickle                 | 15.7 us                                                          | 14.9 us: 1.05x faster                                        |
| async_tree_io_tg         | 900 ms                                                           | 854 ms: 1.05x faster                                         |
| pprint_safe_repr         | 818 ms                                                           | 780 ms: 1.05x faster                                         |
| telco                    | 8.40 ms                                                          | 8.04 ms: 1.04x faster                                        |
| sqlite_synth             | 2.80 us                                                          | 2.68 us: 1.04x faster                                        |
| xml_etree_generate       | 85.7 ms                                                          | 82.4 ms: 1.04x faster                                        |
| scimark_lu               | 97.5 ms                                                          | 93.7 ms: 1.04x faster                                        |
| xml_etree_process        | 59.7 ms                                                          | 57.5 ms: 1.04x faster                                        |
| raytrace                 | 260 ms                                                           | 251 ms: 1.04x faster                                         |
| scimark_fft              | 312 ms                                                           | 301 ms: 1.04x faster                                         |
| create_gc_cycles         | 2.00 ms                                                          | 1.94 ms: 1.03x faster                                        |
| pprint_pformat           | 1.66 sec                                                         | 1.60 sec: 1.03x faster                                       |
| chameleon                | 7.40 ms                                                          | 7.15 ms: 1.03x faster                                        |
| sqlglot_normalize        | 120 ms                                                           | 117 ms: 1.03x faster                                         |
| bench_thread_pool        | 908 us                                                           | 880 us: 1.03x faster                                         |
| genshi_text              | 25.9 ms                                                          | 25.1 ms: 1.03x faster                                        |
| nbody                    | 87.8 ms                                                          | 85.3 ms: 1.03x faster                                        |
| json_dumps               | 10.8 ms                                                          | 10.5 ms: 1.03x faster                                        |
| deepcopy                 | 377 us                                                           | 367 us: 1.03x faster                                         |
| logging_silent           | 96.3 ns                                                          | 93.8 ns: 1.03x faster                                        |
| deepcopy_memo            | 37.3 us                                                          | 36.3 us: 1.03x faster                                        |
| thrift                   | 880 us                                                           | 859 us: 1.02x faster                                         |
| sqlglot_parse            | 1.39 ms                                                          | 1.36 ms: 1.02x faster                                        |
| regex_compile            | 144 ms                                                           | 141 ms: 1.02x faster                                         |
| sqlglot_optimize         | 59.5 ms                                                          | 58.2 ms: 1.02x faster                                        |
| python_startup           | 13.2 ms                                                          | 12.9 ms: 1.02x faster                                        |
| sympy_expand             | 501 ms                                                           | 491 ms: 1.02x faster                                         |
| coverage                 | 83.5 ms                                                          | 81.9 ms: 1.02x faster                                        |
| html5lib                 | 74.7 ms                                                          | 73.2 ms: 1.02x faster                                        |
| async_generators         | 363 ms                                                           | 356 ms: 1.02x faster                                         |
| asyncio_tcp              | 378 ms                                                           | 371 ms: 1.02x faster                                         |
| meteor_contest           | 128 ms                                                           | 126 ms: 1.02x faster                                         |
| chaos                    | 59.6 ms                                                          | 58.6 ms: 1.02x faster                                        |
| scimark_monte_carlo      | 65.5 ms                                                          | 64.4 ms: 1.02x faster                                        |
| scimark_sparse_mat_mult  | 4.28 ms                                                          | 4.21 ms: 1.02x faster                                        |
| crypto_pyaes             | 73.6 ms                                                          | 72.4 ms: 1.02x faster                                        |
| unpickle_list            | 4.70 us                                                          | 4.62 us: 1.02x faster                                        |
| sympy_sum                | 155 ms                                                           | 153 ms: 1.01x faster                                         |
| sympy_str                | 295 ms                                                           | 291 ms: 1.01x faster                                         |
| xml_etree_parse          | 144 ms                                                           | 142 ms: 1.01x faster                                         |
| generators               | 33.5 ms                                                          | 33.1 ms: 1.01x faster                                        |
| sqlglot_transpile        | 1.76 ms                                                          | 1.74 ms: 1.01x faster                                        |
| deepcopy_reduce          | 3.39 us                                                          | 3.35 us: 1.01x faster                                        |
| 2to3                     | 291 ms                                                           | 288 ms: 1.01x faster                                         |
| mako                     | 10.4 ms                                                          | 10.3 ms: 1.01x faster                                        |
| regex_v8                 | 26.0 ms                                                          | 25.7 ms: 1.01x faster                                        |
| gc_traversal             | 4.69 ms                                                          | 4.64 ms: 1.01x faster                                        |
| pickle_pure_python       | 307 us                                                           | 305 us: 1.01x faster                                         |
| comprehensions           | 17.0 us                                                          | 16.8 us: 1.01x faster                                        |
| pickle                   | 10.6 us                                                          | 10.5 us: 1.01x faster                                        |
| docutils                 | 2.98 sec                                                         | 2.97 sec: 1.00x faster                                       |
| asyncio_tcp_ssl          | 1.58 sec                                                         | 1.58 sec: 1.00x faster                                       |
| hexiom                   | 6.35 ms                                                          | 6.38 ms: 1.00x slower                                        |
| deltablue                | 3.37 ms                                                          | 3.39 ms: 1.01x slower                                        |
| pickle_dict              | 32.8 us                                                          | 33.1 us: 1.01x slower                                        |
| xml_etree_iterparse      | 103 ms                                                           | 104 ms: 1.01x slower                                         |
| pickle_list              | 4.44 us                                                          | 4.53 us: 1.02x slower                                        |
| mdp                      | 2.46 sec                                                         | 2.51 sec: 1.02x slower                                       |
| json_loads               | 25.0 us                                                          | 25.6 us: 1.02x slower                                        |
| dulwich_log              | 67.3 ms                                                          | 69.0 ms: 1.02x slower                                        |
| coroutines               | 22.0 ms                                                          | 22.6 ms: 1.03x slower                                        |
| go                       | 165 ms                                                           | 170 ms: 1.03x slower                                         |
| logging_simple           | 6.40 us                                                          | 6.62 us: 1.03x slower                                        |
| pidigits                 | 254 ms                                                           | 263 ms: 1.04x slower                                         |
| pyflate                  | 482 ms                                                           | 500 ms: 1.04x slower                                         |
| json                     | 5.35 ms                                                          | 5.58 ms: 1.04x slower                                        |
| logging_format           | 7.11 us                                                          | 7.41 us: 1.04x slower                                        |
| regex_effbot             | 3.40 ms                                                          | 3.56 ms: 1.05x slower                                        |
| fannkuch                 | 353 ms                                                           | 371 ms: 1.05x slower                                         |
| pathlib                  | 17.1 ms                                                          | 19.2 ms: 1.12x slower                                        |
| scimark_sor              | 119 ms                                                           | 142 ms: 1.19x slower                                         |
| python_startup_no_site   | 8.85 ms                                                          | 11.1 ms: 1.26x slower                                        |
| Geometric mean           | (ref)                                                            | 1.01x faster                                                 |

Benchmark hidden because not significant (16): async_tree_none_tg, async_tree_memoization_tg, gunicorn, async_tree_none, async_tree_memoization, nqueens, aiohttp, pycparser, asyncio_websockets, async_tree_cpu_io_mixed_tg, dask, sympy_integrate, async_tree_cpu_io_mixed, tornado_http, mypy2, async_tree_io
Ignored benchmarks (3) of results/bm-20240605-3.13.0b2-3a83b17/bm-20240605-pythonperf2-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17.json: bpe_tokeniser, django_template, flaskblogging
Ignored benchmarks (1) of results/bm-20240402-3.13.0a5+-c32dc47/bm-20240402-pythonperf2-x86_64-python-main-3.13.0a5+-c32dc47.json: unpack_sequence

# HPT report

- Reliability score: 99.97% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 0.97x