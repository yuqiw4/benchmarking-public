# Results vs. 3.13.0b2

- fork: python
- ref: bfc57d43d8766120ba0c
- machine: linux-x86_64
- commit hash: bfc57d4
- commit date: 2024-03-29
- overall geometric mean: 1.01x faster
- HPT reliability: 94.66%
- HPT 99th percentile: 1.00x faster
- Memory change: 0.97x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240605-pythonperf2-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240329-pythonperf2-x86_64-python-bfc57d43d8766120ba0c-3.13.0a5+-bfc57d4 |
|----------------|:----------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| 2to3           | 291 ms                                                           | 292 ms: 1.00x slower                                                         |
| chameleon      | 7.40 ms                                                          | 7.19 ms: 1.03x faster                                                        |
| docutils       | 2.98 sec                                                         | 2.95 sec: 1.01x faster                                                       |
| html5lib       | 74.7 ms                                                          | 74.0 ms: 1.01x faster                                                        |
| tornado_http   | 119 ms                                                           | 121 ms: 1.02x slower                                                         |
| Geometric mean | (ref)                                                            | 1.01x faster                                                                 |

Benchmarks with tag 'asyncio':
==============================

| Benchmark               | bm-20240605-pythonperf2-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240329-pythonperf2-x86_64-python-bfc57d43d8766120ba0c-3.13.0a5+-bfc57d4 |
|-------------------------|:----------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| async_tree_io_tg        | 900 ms                                                           | 854 ms: 1.05x faster                                                         |
| async_tree_cpu_io_mixed | 604 ms                                                           | 594 ms: 1.02x faster                                                         |
| async_tree_io           | 873 ms                                                           | 893 ms: 1.02x slower                                                         |
| async_tree_none         | 365 ms                                                           | 376 ms: 1.03x slower                                                         |
| Geometric mean          | (ref)                                                            | 1.00x faster                                                                 |

Benchmark hidden because not significant (4): async_tree_memoization, async_tree_none_tg, async_tree_memoization_tg, async_tree_cpu_io_mixed_tg

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240605-pythonperf2-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240329-pythonperf2-x86_64-python-bfc57d43d8766120ba0c-3.13.0a5+-bfc57d4 |
|----------------|:----------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| float          | 80.2 ms                                                          | 76.5 ms: 1.05x faster                                                        |
| pidigits       | 254 ms                                                           | 263 ms: 1.04x slower                                                         |
| Geometric mean | (ref)                                                            | 1.01x faster                                                                 |

Benchmark hidden because not significant (1): nbody

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240605-pythonperf2-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240329-pythonperf2-x86_64-python-bfc57d43d8766120ba0c-3.13.0a5+-bfc57d4 |
|----------------|:----------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| regex_compile  | 144 ms                                                           | 142 ms: 1.01x faster                                                         |
| regex_v8       | 26.0 ms                                                          | 25.7 ms: 1.01x faster                                                        |
| regex_dna      | 249 ms                                                           | 249 ms: 1.00x faster                                                         |
| regex_effbot   | 3.40 ms                                                          | 3.55 ms: 1.04x slower                                                        |
| Geometric mean | (ref)                                                            | 1.00x slower                                                                 |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240605-pythonperf2-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240329-pythonperf2-x86_64-python-bfc57d43d8766120ba0c-3.13.0a5+-bfc57d4 |
|----------------------|:----------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| unpickle             | 15.7 us                                                          | 14.7 us: 1.07x faster                                                        |
| unpickle_pure_python | 224 us                                                           | 213 us: 1.05x faster                                                         |
| tomli_loads          | 2.40 sec                                                         | 2.30 sec: 1.04x faster                                                       |
| json_dumps           | 10.8 ms                                                          | 10.5 ms: 1.03x faster                                                        |
| xml_etree_process    | 59.7 ms                                                          | 58.4 ms: 1.02x faster                                                        |
| unpickle_list        | 4.70 us                                                          | 4.61 us: 1.02x faster                                                        |
| xml_etree_generate   | 85.7 ms                                                          | 84.2 ms: 1.02x faster                                                        |
| pickle               | 10.6 us                                                          | 10.5 us: 1.01x faster                                                        |
| pickle_pure_python   | 307 us                                                           | 306 us: 1.00x faster                                                         |
| pickle_list          | 4.44 us                                                          | 4.47 us: 1.01x slower                                                        |
| json_loads           | 25.0 us                                                          | 25.5 us: 1.02x slower                                                        |
| pickle_dict          | 32.8 us                                                          | 33.7 us: 1.03x slower                                                        |
| Geometric mean       | (ref)                                                            | 1.02x faster                                                                 |

Benchmark hidden because not significant (2): xml_etree_parse, xml_etree_iterparse

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240605-pythonperf2-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240329-pythonperf2-x86_64-python-bfc57d43d8766120ba0c-3.13.0a5+-bfc57d4 |
|------------------------|:----------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| python_startup         | 13.2 ms                                                          | 12.8 ms: 1.03x faster                                                        |
| python_startup_no_site | 8.85 ms                                                          | 11.1 ms: 1.25x slower                                                        |
| Geometric mean         | (ref)                                                            | 1.10x slower                                                                 |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240605-pythonperf2-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240329-pythonperf2-x86_64-python-bfc57d43d8766120ba0c-3.13.0a5+-bfc57d4 |
|-----------------|:----------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| genshi_xml      | 58.1 ms                                                          | 53.8 ms: 1.08x faster                                                        |
| genshi_text     | 25.9 ms                                                          | 24.8 ms: 1.04x faster                                                        |
| mako            | 10.4 ms                                                          | 10.2 ms: 1.02x faster                                                        |
| django_template | 39.0 ms                                                          | 38.5 ms: 1.01x faster                                                        |
| Geometric mean  | (ref)                                                            | 1.04x faster                                                                 |

All benchmarks:
===============

| Benchmark                | bm-20240605-pythonperf2-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240329-pythonperf2-x86_64-python-bfc57d43d8766120ba0c-3.13.0a5+-bfc57d4 |
|--------------------------|:----------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| typing_runtime_protocols | 171 us                                                           | 115 us: 1.48x faster                                                         |
| create_gc_cycles         | 2.00 ms                                                          | 1.81 ms: 1.11x faster                                                        |
| genshi_xml               | 58.1 ms                                                          | 53.8 ms: 1.08x faster                                                        |
| bench_mp_pool            | 4.91 ms                                                          | 4.59 ms: 1.07x faster                                                        |
| unpickle                 | 15.7 us                                                          | 14.7 us: 1.07x faster                                                        |
| telco                    | 8.40 ms                                                          | 7.91 ms: 1.06x faster                                                        |
| pylint                   | 339 ms                                                           | 320 ms: 1.06x faster                                                         |
| scimark_fft              | 312 ms                                                           | 296 ms: 1.05x faster                                                         |
| unpickle_pure_python     | 224 us                                                           | 213 us: 1.05x faster                                                         |
| async_tree_io_tg         | 900 ms                                                           | 854 ms: 1.05x faster                                                         |
| spectral_norm            | 97.3 ms                                                          | 92.7 ms: 1.05x faster                                                        |
| float                    | 80.2 ms                                                          | 76.5 ms: 1.05x faster                                                        |
| tomli_loads              | 2.40 sec                                                         | 2.30 sec: 1.04x faster                                                       |
| genshi_text              | 25.9 ms                                                          | 24.8 ms: 1.04x faster                                                        |
| pprint_safe_repr         | 818 ms                                                           | 785 ms: 1.04x faster                                                         |
| pprint_pformat           | 1.66 sec                                                         | 1.60 sec: 1.03x faster                                                       |
| scimark_sparse_mat_mult  | 4.28 ms                                                          | 4.14 ms: 1.03x faster                                                        |
| richards_super           | 61.2 ms                                                          | 59.3 ms: 1.03x faster                                                        |
| sqlglot_normalize        | 120 ms                                                           | 117 ms: 1.03x faster                                                         |
| python_startup           | 13.2 ms                                                          | 12.8 ms: 1.03x faster                                                        |
| chameleon                | 7.40 ms                                                          | 7.19 ms: 1.03x faster                                                        |
| json_dumps               | 10.8 ms                                                          | 10.5 ms: 1.03x faster                                                        |
| crypto_pyaes             | 73.6 ms                                                          | 71.7 ms: 1.03x faster                                                        |
| aiohttp                  | 1.07 ms                                                          | 1.05 ms: 1.02x faster                                                        |
| xml_etree_process        | 59.7 ms                                                          | 58.4 ms: 1.02x faster                                                        |
| sympy_sum                | 155 ms                                                           | 151 ms: 1.02x faster                                                         |
| sqlite_synth             | 2.80 us                                                          | 2.74 us: 1.02x faster                                                        |
| mako                     | 10.4 ms                                                          | 10.2 ms: 1.02x faster                                                        |
| scimark_lu               | 97.5 ms                                                          | 95.6 ms: 1.02x faster                                                        |
| asyncio_tcp              | 378 ms                                                           | 371 ms: 1.02x faster                                                         |
| unpickle_list            | 4.70 us                                                          | 4.61 us: 1.02x faster                                                        |
| sqlglot_optimize         | 59.5 ms                                                          | 58.4 ms: 1.02x faster                                                        |
| sympy_str                | 295 ms                                                           | 290 ms: 1.02x faster                                                         |
| xml_etree_generate       | 85.7 ms                                                          | 84.2 ms: 1.02x faster                                                        |
| async_tree_cpu_io_mixed  | 604 ms                                                           | 594 ms: 1.02x faster                                                         |
| thrift                   | 880 us                                                           | 865 us: 1.02x faster                                                         |
| deepcopy_memo            | 37.3 us                                                          | 36.7 us: 1.01x faster                                                        |
| regex_compile            | 144 ms                                                           | 142 ms: 1.01x faster                                                         |
| meteor_contest           | 128 ms                                                           | 126 ms: 1.01x faster                                                         |
| sqlglot_parse            | 1.39 ms                                                          | 1.37 ms: 1.01x faster                                                        |
| django_template          | 39.0 ms                                                          | 38.5 ms: 1.01x faster                                                        |
| regex_v8                 | 26.0 ms                                                          | 25.7 ms: 1.01x faster                                                        |
| sympy_expand             | 501 ms                                                           | 495 ms: 1.01x faster                                                         |
| asyncio_websockets       | 395 ms                                                           | 391 ms: 1.01x faster                                                         |
| sqlglot_transpile        | 1.76 ms                                                          | 1.75 ms: 1.01x faster                                                        |
| docutils                 | 2.98 sec                                                         | 2.95 sec: 1.01x faster                                                       |
| scimark_monte_carlo      | 65.5 ms                                                          | 64.9 ms: 1.01x faster                                                        |
| async_generators         | 363 ms                                                           | 360 ms: 1.01x faster                                                         |
| html5lib                 | 74.7 ms                                                          | 74.0 ms: 1.01x faster                                                        |
| pickle                   | 10.6 us                                                          | 10.5 us: 1.01x faster                                                        |
| deepcopy_reduce          | 3.39 us                                                          | 3.37 us: 1.01x faster                                                        |
| comprehensions           | 17.0 us                                                          | 16.9 us: 1.01x faster                                                        |
| asyncio_tcp_ssl          | 1.58 sec                                                         | 1.57 sec: 1.01x faster                                                       |
| pickle_pure_python       | 307 us                                                           | 306 us: 1.00x faster                                                         |
| regex_dna                | 249 ms                                                           | 249 ms: 1.00x faster                                                         |
| generators               | 33.5 ms                                                          | 33.4 ms: 1.00x faster                                                        |
| 2to3                     | 291 ms                                                           | 292 ms: 1.00x slower                                                         |
| pickle_list              | 4.44 us                                                          | 4.47 us: 1.01x slower                                                        |
| chaos                    | 59.6 ms                                                          | 60.0 ms: 1.01x slower                                                        |
| deepcopy                 | 377 us                                                           | 381 us: 1.01x slower                                                         |
| hexiom                   | 6.35 ms                                                          | 6.41 ms: 1.01x slower                                                        |
| tornado_http             | 119 ms                                                           | 121 ms: 1.02x slower                                                         |
| json_loads               | 25.0 us                                                          | 25.5 us: 1.02x slower                                                        |
| coverage                 | 83.5 ms                                                          | 85.0 ms: 1.02x slower                                                        |
| coroutines               | 22.0 ms                                                          | 22.4 ms: 1.02x slower                                                        |
| logging_simple           | 6.40 us                                                          | 6.53 us: 1.02x slower                                                        |
| dulwich_log              | 67.3 ms                                                          | 68.7 ms: 1.02x slower                                                        |
| async_tree_io            | 873 ms                                                           | 893 ms: 1.02x slower                                                         |
| mdp                      | 2.46 sec                                                         | 2.52 sec: 1.02x slower                                                       |
| pickle_dict              | 32.8 us                                                          | 33.7 us: 1.03x slower                                                        |
| async_tree_none          | 365 ms                                                           | 376 ms: 1.03x slower                                                         |
| pidigits                 | 254 ms                                                           | 263 ms: 1.04x slower                                                         |
| go                       | 165 ms                                                           | 172 ms: 1.04x slower                                                         |
| regex_effbot             | 3.40 ms                                                          | 3.55 ms: 1.04x slower                                                        |
| pycparser                | 1.22 sec                                                         | 1.29 sec: 1.05x slower                                                       |
| deltablue                | 3.37 ms                                                          | 3.57 ms: 1.06x slower                                                        |
| fannkuch                 | 353 ms                                                           | 382 ms: 1.08x slower                                                         |
| pyflate                  | 482 ms                                                           | 535 ms: 1.11x slower                                                         |
| pathlib                  | 17.1 ms                                                          | 19.4 ms: 1.14x slower                                                        |
| scimark_sor              | 119 ms                                                           | 144 ms: 1.21x slower                                                         |
| python_startup_no_site   | 8.85 ms                                                          | 11.1 ms: 1.25x slower                                                        |
| Geometric mean           | (ref)                                                            | 1.01x faster                                                                 |

Benchmark hidden because not significant (19): async_tree_memoization, nqueens, async_tree_none_tg, nbody, bench_thread_pool, json, gc_traversal, xml_etree_parse, xml_etree_iterparse, sympy_integrate, logging_silent, logging_format, gunicorn, raytrace, richards, mypy2, dask, async_tree_memoization_tg, async_tree_cpu_io_mixed_tg
Ignored benchmarks (2) of results/bm-20240605-3.13.0b2-3a83b17/bm-20240605-pythonperf2-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17.json: bpe_tokeniser, flaskblogging
Ignored benchmarks (1) of results/bm-20240329-3.13.0a5+-bfc57d4/bm-20240329-pythonperf2-x86_64-python-bfc57d43d8766120ba0c-3.13.0a5+-bfc57d4.json: unpack_sequence

# HPT report

- Reliability score: 94.66% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 0.97x