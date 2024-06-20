# Results vs. 3.13.0b2

- fork: savannahostrowski
- ref: llvm_18
- machine: linux-x86_64
- commit hash: 8d9855f
- commit date: 2024-04-26
- overall geometric mean: 1.02x slower
- HPT reliability: 99.98%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.07x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240605-pythonperf2-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240426-pythonperf2-x86_64-savannahostrowski-llvm_18-3.13.0a6+-8d9855f |
|----------------|:----------------------------------------------------------------:|:--------------------------------------------------------------------------:|
| 2to3           | 291 ms                                                           | 302 ms: 1.03x slower                                                       |
| chameleon      | 7.40 ms                                                          | 7.46 ms: 1.01x slower                                                      |
| docutils       | 2.98 sec                                                         | 3.09 sec: 1.03x slower                                                     |
| tornado_http   | 119 ms                                                           | 122 ms: 1.02x slower                                                       |
| Geometric mean | (ref)                                                            | 1.02x slower                                                               |

Benchmark hidden because not significant (1): html5lib

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240605-pythonperf2-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240426-pythonperf2-x86_64-savannahostrowski-llvm_18-3.13.0a6+-8d9855f |
|----------------------------|:----------------------------------------------------------------:|:--------------------------------------------------------------------------:|
| async_tree_io_tg           | 900 ms                                                           | 852 ms: 1.06x faster                                                       |
| async_tree_none            | 365 ms                                                           | 371 ms: 1.02x slower                                                       |
| async_tree_cpu_io_mixed    | 604 ms                                                           | 614 ms: 1.02x slower                                                       |
| async_tree_cpu_io_mixed_tg | 573 ms                                                           | 589 ms: 1.03x slower                                                       |
| Geometric mean             | (ref)                                                            | 1.00x slower                                                               |

Benchmark hidden because not significant (4): async_tree_none_tg, async_tree_memoization_tg, async_tree_memoization, async_tree_io

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240605-pythonperf2-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240426-pythonperf2-x86_64-savannahostrowski-llvm_18-3.13.0a6+-8d9855f |
|----------------|:----------------------------------------------------------------:|:--------------------------------------------------------------------------:|
| float          | 80.2 ms                                                          | 76.0 ms: 1.06x faster                                                      |
| pidigits       | 254 ms                                                           | 261 ms: 1.03x slower                                                       |
| nbody          | 87.8 ms                                                          | 98.9 ms: 1.13x slower                                                      |
| Geometric mean | (ref)                                                            | 1.03x slower                                                               |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240605-pythonperf2-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240426-pythonperf2-x86_64-savannahostrowski-llvm_18-3.13.0a6+-8d9855f |
|----------------|:----------------------------------------------------------------:|:--------------------------------------------------------------------------:|
| regex_dna      | 249 ms                                                           | 238 ms: 1.05x faster                                                       |
| regex_compile  | 144 ms                                                           | 143 ms: 1.01x faster                                                       |
| regex_v8       | 26.0 ms                                                          | 26.1 ms: 1.00x slower                                                      |
| regex_effbot   | 3.40 ms                                                          | 3.51 ms: 1.03x slower                                                      |
| Geometric mean | (ref)                                                            | 1.00x faster                                                               |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240605-pythonperf2-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240426-pythonperf2-x86_64-savannahostrowski-llvm_18-3.13.0a6+-8d9855f |
|----------------------|:----------------------------------------------------------------:|:--------------------------------------------------------------------------:|
| tomli_loads          | 2.40 sec                                                         | 2.09 sec: 1.15x faster                                                     |
| pickle_dict          | 32.8 us                                                          | 30.5 us: 1.08x faster                                                      |
| unpickle_pure_python | 224 us                                                           | 214 us: 1.05x faster                                                       |
| xml_etree_process    | 59.7 ms                                                          | 57.6 ms: 1.04x faster                                                      |
| xml_etree_generate   | 85.7 ms                                                          | 83.0 ms: 1.03x faster                                                      |
| pickle               | 10.6 us                                                          | 10.3 us: 1.03x faster                                                      |
| xml_etree_iterparse  | 103 ms                                                           | 100 ms: 1.02x faster                                                       |
| json_loads           | 25.0 us                                                          | 24.6 us: 1.02x faster                                                      |
| json_dumps           | 10.8 ms                                                          | 10.7 ms: 1.01x faster                                                      |
| xml_etree_parse      | 144 ms                                                           | 142 ms: 1.01x faster                                                       |
| pickle_list          | 4.44 us                                                          | 4.50 us: 1.01x slower                                                      |
| pickle_pure_python   | 307 us                                                           | 317 us: 1.03x slower                                                       |
| Geometric mean       | (ref)                                                            | 1.03x faster                                                               |

Benchmark hidden because not significant (2): unpickle, unpickle_list

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240605-pythonperf2-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240426-pythonperf2-x86_64-savannahostrowski-llvm_18-3.13.0a6+-8d9855f |
|------------------------|:----------------------------------------------------------------:|:--------------------------------------------------------------------------:|
| python_startup         | 13.2 ms                                                          | 13.4 ms: 1.02x slower                                                      |
| python_startup_no_site | 8.85 ms                                                          | 9.43 ms: 1.07x slower                                                      |
| Geometric mean         | (ref)                                                            | 1.04x slower                                                               |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240605-pythonperf2-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240426-pythonperf2-x86_64-savannahostrowski-llvm_18-3.13.0a6+-8d9855f |
|-----------------|:----------------------------------------------------------------:|:--------------------------------------------------------------------------:|
| mako            | 10.4 ms                                                          | 9.65 ms: 1.07x faster                                                      |
| django_template | 39.0 ms                                                          | 40.4 ms: 1.04x slower                                                      |
| genshi_xml      | 58.1 ms                                                          | 62.3 ms: 1.07x slower                                                      |
| genshi_text     | 25.9 ms                                                          | 29.1 ms: 1.12x slower                                                      |
| Geometric mean  | (ref)                                                            | 1.04x slower                                                               |

All benchmarks:
===============

| Benchmark                  | bm-20240605-pythonperf2-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240426-pythonperf2-x86_64-savannahostrowski-llvm_18-3.13.0a6+-8d9855f |
|----------------------------|:----------------------------------------------------------------:|:--------------------------------------------------------------------------:|
| richards_super             | 61.2 ms                                                          | 51.2 ms: 1.19x faster                                                      |
| richards                   | 53.4 ms                                                          | 45.8 ms: 1.17x faster                                                      |
| tomli_loads                | 2.40 sec                                                         | 2.09 sec: 1.15x faster                                                     |
| pickle_dict                | 32.8 us                                                          | 30.5 us: 1.08x faster                                                      |
| mako                       | 10.4 ms                                                          | 9.65 ms: 1.07x faster                                                      |
| spectral_norm              | 97.3 ms                                                          | 90.9 ms: 1.07x faster                                                      |
| create_gc_cycles           | 2.00 ms                                                          | 1.89 ms: 1.06x faster                                                      |
| gc_traversal               | 4.69 ms                                                          | 4.43 ms: 1.06x faster                                                      |
| async_tree_io_tg           | 900 ms                                                           | 852 ms: 1.06x faster                                                       |
| float                      | 80.2 ms                                                          | 76.0 ms: 1.06x faster                                                      |
| scimark_sparse_mat_mult    | 4.28 ms                                                          | 4.06 ms: 1.05x faster                                                      |
| unpickle_pure_python       | 224 us                                                           | 214 us: 1.05x faster                                                       |
| regex_dna                  | 249 ms                                                           | 238 ms: 1.05x faster                                                       |
| coverage                   | 83.5 ms                                                          | 79.6 ms: 1.05x faster                                                      |
| telco                      | 8.40 ms                                                          | 8.05 ms: 1.04x faster                                                      |
| xml_etree_process          | 59.7 ms                                                          | 57.6 ms: 1.04x faster                                                      |
| xml_etree_generate         | 85.7 ms                                                          | 83.0 ms: 1.03x faster                                                      |
| sqlite_synth               | 2.80 us                                                          | 2.71 us: 1.03x faster                                                      |
| pickle                     | 10.6 us                                                          | 10.3 us: 1.03x faster                                                      |
| xml_etree_iterparse        | 103 ms                                                           | 100 ms: 1.02x faster                                                       |
| json_loads                 | 25.0 us                                                          | 24.6 us: 1.02x faster                                                      |
| coroutines                 | 22.0 ms                                                          | 21.6 ms: 1.02x faster                                                      |
| json_dumps                 | 10.8 ms                                                          | 10.7 ms: 1.01x faster                                                      |
| xml_etree_parse            | 144 ms                                                           | 142 ms: 1.01x faster                                                       |
| asyncio_tcp                | 378 ms                                                           | 374 ms: 1.01x faster                                                       |
| asyncio_websockets         | 395 ms                                                           | 391 ms: 1.01x faster                                                       |
| logging_silent             | 96.3 ns                                                          | 95.4 ns: 1.01x faster                                                      |
| json                       | 5.35 ms                                                          | 5.31 ms: 1.01x faster                                                      |
| regex_compile              | 144 ms                                                           | 143 ms: 1.01x faster                                                       |
| asyncio_tcp_ssl            | 1.58 sec                                                         | 1.58 sec: 1.00x faster                                                     |
| regex_v8                   | 26.0 ms                                                          | 26.1 ms: 1.00x slower                                                      |
| logging_format             | 7.11 us                                                          | 7.15 us: 1.01x slower                                                      |
| chameleon                  | 7.40 ms                                                          | 7.46 ms: 1.01x slower                                                      |
| pprint_pformat             | 1.66 sec                                                         | 1.68 sec: 1.01x slower                                                     |
| pickle_list                | 4.44 us                                                          | 4.50 us: 1.01x slower                                                      |
| deepcopy_reduce            | 3.39 us                                                          | 3.44 us: 1.02x slower                                                      |
| async_tree_none            | 365 ms                                                           | 371 ms: 1.02x slower                                                       |
| python_startup             | 13.2 ms                                                          | 13.4 ms: 1.02x slower                                                      |
| async_tree_cpu_io_mixed    | 604 ms                                                           | 614 ms: 1.02x slower                                                       |
| logging_simple             | 6.40 us                                                          | 6.52 us: 1.02x slower                                                      |
| tornado_http               | 119 ms                                                           | 122 ms: 1.02x slower                                                       |
| sqlglot_parse              | 1.39 ms                                                          | 1.42 ms: 1.02x slower                                                      |
| sqlglot_normalize          | 120 ms                                                           | 123 ms: 1.02x slower                                                       |
| sympy_expand               | 501 ms                                                           | 513 ms: 1.02x slower                                                       |
| pathlib                    | 17.1 ms                                                          | 17.6 ms: 1.03x slower                                                      |
| pprint_safe_repr           | 818 ms                                                           | 839 ms: 1.03x slower                                                       |
| pyflate                    | 482 ms                                                           | 494 ms: 1.03x slower                                                       |
| generators                 | 33.5 ms                                                          | 34.4 ms: 1.03x slower                                                      |
| dask                       | 391 ms                                                           | 402 ms: 1.03x slower                                                       |
| async_tree_cpu_io_mixed_tg | 573 ms                                                           | 589 ms: 1.03x slower                                                       |
| pidigits                   | 254 ms                                                           | 261 ms: 1.03x slower                                                       |
| pickle_pure_python         | 307 us                                                           | 317 us: 1.03x slower                                                       |
| regex_effbot               | 3.40 ms                                                          | 3.51 ms: 1.03x slower                                                      |
| sqlglot_transpile          | 1.76 ms                                                          | 1.82 ms: 1.03x slower                                                      |
| docutils                   | 2.98 sec                                                         | 3.09 sec: 1.03x slower                                                     |
| 2to3                       | 291 ms                                                           | 302 ms: 1.03x slower                                                       |
| bench_thread_pool          | 908 us                                                           | 941 us: 1.04x slower                                                       |
| django_template            | 39.0 ms                                                          | 40.4 ms: 1.04x slower                                                      |
| crypto_pyaes               | 73.6 ms                                                          | 76.3 ms: 1.04x slower                                                      |
| deepcopy                   | 377 us                                                           | 393 us: 1.04x slower                                                       |
| mdp                        | 2.46 sec                                                         | 2.57 sec: 1.04x slower                                                     |
| sympy_str                  | 295 ms                                                           | 308 ms: 1.04x slower                                                       |
| go                         | 165 ms                                                           | 173 ms: 1.05x slower                                                       |
| gunicorn                   | 1.04 ms                                                          | 1.10 ms: 1.05x slower                                                      |
| aiohttp                    | 1.07 ms                                                          | 1.13 ms: 1.05x slower                                                      |
| meteor_contest             | 128 ms                                                           | 135 ms: 1.06x slower                                                       |
| scimark_monte_carlo        | 65.5 ms                                                          | 69.1 ms: 1.06x slower                                                      |
| pycparser                  | 1.22 sec                                                         | 1.29 sec: 1.06x slower                                                     |
| sqlglot_optimize           | 59.5 ms                                                          | 63.1 ms: 1.06x slower                                                      |
| sympy_sum                  | 155 ms                                                           | 165 ms: 1.06x slower                                                       |
| fannkuch                   | 353 ms                                                           | 376 ms: 1.06x slower                                                       |
| python_startup_no_site     | 8.85 ms                                                          | 9.43 ms: 1.07x slower                                                      |
| async_generators           | 363 ms                                                           | 389 ms: 1.07x slower                                                       |
| genshi_xml                 | 58.1 ms                                                          | 62.3 ms: 1.07x slower                                                      |
| raytrace                   | 260 ms                                                           | 281 ms: 1.08x slower                                                       |
| typing_runtime_protocols   | 171 us                                                           | 185 us: 1.08x slower                                                       |
| pylint                     | 339 ms                                                           | 370 ms: 1.09x slower                                                       |
| chaos                      | 59.6 ms                                                          | 65.7 ms: 1.10x slower                                                      |
| mypy2                      | 764 ms                                                           | 843 ms: 1.10x slower                                                       |
| sympy_integrate            | 23.2 ms                                                          | 25.6 ms: 1.10x slower                                                      |
| hexiom                     | 6.35 ms                                                          | 7.02 ms: 1.10x slower                                                      |
| genshi_text                | 25.9 ms                                                          | 29.1 ms: 1.12x slower                                                      |
| deltablue                  | 3.37 ms                                                          | 3.80 ms: 1.13x slower                                                      |
| nbody                      | 87.8 ms                                                          | 98.9 ms: 1.13x slower                                                      |
| nqueens                    | 88.4 ms                                                          | 100 ms: 1.13x slower                                                       |
| comprehensions             | 17.0 us                                                          | 19.3 us: 1.14x slower                                                      |
| scimark_lu                 | 97.5 ms                                                          | 119 ms: 1.23x slower                                                       |
| scimark_sor                | 119 ms                                                           | 151 ms: 1.27x slower                                                       |
| Geometric mean             | (ref)                                                            | 1.02x slower                                                               |

Benchmark hidden because not significant (12): bench_mp_pool, async_tree_none_tg, async_tree_memoization_tg, thrift, unpickle, html5lib, dulwich_log, deepcopy_memo, unpickle_list, async_tree_memoization, async_tree_io, scimark_fft
Ignored benchmarks (2) of results/bm-20240605-3.13.0b2-3a83b17/bm-20240605-pythonperf2-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17.json: bpe_tokeniser, flaskblogging

# HPT report

- Reliability score: 99.98% likely to be slow
- 90% likely to have a slowdown of 1.01x
- 95% likely to have a slowdown of 1.01x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.07x