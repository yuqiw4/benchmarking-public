# Results vs. 3.13.0b2

- fork: mdboom
- ref: all_above_200
- machine: linux-x86_64
- commit hash: d42ae28
- commit date: 2024-04-03
- overall geometric mean: 1.03x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.02x slower
- Memory change: 1.05x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240605-pythonperf2-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240403-pythonperf2-x86_64-mdboom-all_above_200-3.13.0a5+-d42ae28 |
|----------------|:----------------------------------------------------------------:|:---------------------------------------------------------------------:|
| 2to3           | 291 ms                                                           | 302 ms: 1.04x slower                                                  |
| chameleon      | 7.40 ms                                                          | 7.31 ms: 1.01x faster                                                 |
| docutils       | 2.98 sec                                                         | 3.06 sec: 1.03x slower                                                |
| html5lib       | 74.7 ms                                                          | 72.5 ms: 1.03x faster                                                 |
| tornado_http   | 119 ms                                                           | 124 ms: 1.03x slower                                                  |
| Geometric mean | (ref)                                                            | 1.01x slower                                                          |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240605-pythonperf2-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240403-pythonperf2-x86_64-mdboom-all_above_200-3.13.0a5+-d42ae28 |
|----------------------------|:----------------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_io_tg           | 900 ms                                                           | 879 ms: 1.02x faster                                                  |
| async_tree_none            | 365 ms                                                           | 377 ms: 1.03x slower                                                  |
| async_tree_cpu_io_mixed_tg | 573 ms                                                           | 592 ms: 1.03x slower                                                  |
| async_tree_io              | 873 ms                                                           | 906 ms: 1.04x slower                                                  |
| Geometric mean             | (ref)                                                            | 1.01x slower                                                          |

Benchmark hidden because not significant (4): async_tree_memoization, async_tree_none_tg, async_tree_cpu_io_mixed, async_tree_memoization_tg

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240605-pythonperf2-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240403-pythonperf2-x86_64-mdboom-all_above_200-3.13.0a5+-d42ae28 |
|----------------|:----------------------------------------------------------------:|:---------------------------------------------------------------------:|
| float          | 80.2 ms                                                          | 77.7 ms: 1.03x faster                                                 |
| pidigits       | 254 ms                                                           | 264 ms: 1.04x slower                                                  |
| nbody          | 87.8 ms                                                          | 94.7 ms: 1.08x slower                                                 |
| Geometric mean | (ref)                                                            | 1.03x slower                                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240605-pythonperf2-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240403-pythonperf2-x86_64-mdboom-all_above_200-3.13.0a5+-d42ae28 |
|----------------|:----------------------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_dna      | 249 ms                                                           | 247 ms: 1.01x faster                                                  |
| regex_v8       | 26.0 ms                                                          | 25.9 ms: 1.00x faster                                                 |
| regex_effbot   | 3.40 ms                                                          | 3.50 ms: 1.03x slower                                                 |
| regex_compile  | 144 ms                                                           | 150 ms: 1.04x slower                                                  |
| Geometric mean | (ref)                                                            | 1.01x slower                                                          |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240605-pythonperf2-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240403-pythonperf2-x86_64-mdboom-all_above_200-3.13.0a5+-d42ae28 |
|----------------------|:----------------------------------------------------------------:|:---------------------------------------------------------------------:|
| tomli_loads          | 2.40 sec                                                         | 2.21 sec: 1.09x faster                                                |
| unpickle             | 15.7 us                                                          | 14.6 us: 1.07x faster                                                 |
| unpickle_list        | 4.70 us                                                          | 4.60 us: 1.02x faster                                                 |
| xml_etree_process    | 59.7 ms                                                          | 58.9 ms: 1.01x faster                                                 |
| json_dumps           | 10.8 ms                                                          | 10.7 ms: 1.01x faster                                                 |
| xml_etree_generate   | 85.7 ms                                                          | 85.5 ms: 1.00x faster                                                 |
| pickle_pure_python   | 307 us                                                           | 310 us: 1.01x slower                                                  |
| pickle_dict          | 32.8 us                                                          | 33.1 us: 1.01x slower                                                 |
| xml_etree_iterparse  | 103 ms                                                           | 104 ms: 1.01x slower                                                  |
| xml_etree_parse      | 144 ms                                                           | 146 ms: 1.02x slower                                                  |
| json_loads           | 25.0 us                                                          | 25.8 us: 1.03x slower                                                 |
| pickle               | 10.6 us                                                          | 11.1 us: 1.05x slower                                                 |
| unpickle_pure_python | 224 us                                                           | 241 us: 1.07x slower                                                  |
| Geometric mean       | (ref)                                                            | 1.00x faster                                                          |

Benchmark hidden because not significant (1): pickle_list

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240605-pythonperf2-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240403-pythonperf2-x86_64-mdboom-all_above_200-3.13.0a5+-d42ae28 |
|------------------------|:----------------------------------------------------------------:|:---------------------------------------------------------------------:|
| python_startup         | 13.2 ms                                                          | 13.6 ms: 1.03x slower                                                 |
| python_startup_no_site | 8.85 ms                                                          | 11.8 ms: 1.33x slower                                                 |
| Geometric mean         | (ref)                                                            | 1.17x slower                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240605-pythonperf2-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240403-pythonperf2-x86_64-mdboom-all_above_200-3.13.0a5+-d42ae28 |
|-----------------|:----------------------------------------------------------------:|:---------------------------------------------------------------------:|
| mako            | 10.4 ms                                                          | 9.84 ms: 1.05x faster                                                 |
| django_template | 39.0 ms                                                          | 40.1 ms: 1.03x slower                                                 |
| genshi_text     | 25.9 ms                                                          | 27.7 ms: 1.07x slower                                                 |
| genshi_xml      | 58.1 ms                                                          | 62.7 ms: 1.08x slower                                                 |
| Geometric mean  | (ref)                                                            | 1.03x slower                                                          |

All benchmarks:
===============

| Benchmark                  | bm-20240605-pythonperf2-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240403-pythonperf2-x86_64-mdboom-all_above_200-3.13.0a5+-d42ae28 |
|----------------------------|:----------------------------------------------------------------:|:---------------------------------------------------------------------:|
| typing_runtime_protocols   | 171 us                                                           | 123 us: 1.39x faster                                                  |
| create_gc_cycles           | 2.00 ms                                                          | 1.81 ms: 1.11x faster                                                 |
| tomli_loads                | 2.40 sec                                                         | 2.21 sec: 1.09x faster                                                |
| unpickle                   | 15.7 us                                                          | 14.6 us: 1.07x faster                                                 |
| mako                       | 10.4 ms                                                          | 9.84 ms: 1.05x faster                                                 |
| richards                   | 53.4 ms                                                          | 51.2 ms: 1.04x faster                                                 |
| thrift                     | 880 us                                                           | 845 us: 1.04x faster                                                  |
| richards_super             | 61.2 ms                                                          | 58.9 ms: 1.04x faster                                                 |
| sqlite_synth               | 2.80 us                                                          | 2.70 us: 1.04x faster                                                 |
| scimark_sparse_mat_mult    | 4.28 ms                                                          | 4.14 ms: 1.03x faster                                                 |
| float                      | 80.2 ms                                                          | 77.7 ms: 1.03x faster                                                 |
| html5lib                   | 74.7 ms                                                          | 72.5 ms: 1.03x faster                                                 |
| telco                      | 8.40 ms                                                          | 8.19 ms: 1.03x faster                                                 |
| async_tree_io_tg           | 900 ms                                                           | 879 ms: 1.02x faster                                                  |
| asyncio_tcp                | 378 ms                                                           | 369 ms: 1.02x faster                                                  |
| coverage                   | 83.5 ms                                                          | 81.6 ms: 1.02x faster                                                 |
| unpickle_list              | 4.70 us                                                          | 4.60 us: 1.02x faster                                                 |
| asyncio_websockets         | 395 ms                                                           | 387 ms: 1.02x faster                                                  |
| xml_etree_process          | 59.7 ms                                                          | 58.9 ms: 1.01x faster                                                 |
| chameleon                  | 7.40 ms                                                          | 7.31 ms: 1.01x faster                                                 |
| spectral_norm              | 97.3 ms                                                          | 96.2 ms: 1.01x faster                                                 |
| regex_dna                  | 249 ms                                                           | 247 ms: 1.01x faster                                                  |
| json_dumps                 | 10.8 ms                                                          | 10.7 ms: 1.01x faster                                                 |
| regex_v8                   | 26.0 ms                                                          | 25.9 ms: 1.00x faster                                                 |
| asyncio_tcp_ssl            | 1.58 sec                                                         | 1.58 sec: 1.00x faster                                                |
| xml_etree_generate         | 85.7 ms                                                          | 85.5 ms: 1.00x faster                                                 |
| pickle_pure_python         | 307 us                                                           | 310 us: 1.01x slower                                                  |
| pickle_dict                | 32.8 us                                                          | 33.1 us: 1.01x slower                                                 |
| logging_silent             | 96.3 ns                                                          | 97.3 ns: 1.01x slower                                                 |
| pprint_safe_repr           | 818 ms                                                           | 828 ms: 1.01x slower                                                  |
| json                       | 5.35 ms                                                          | 5.42 ms: 1.01x slower                                                 |
| xml_etree_iterparse        | 103 ms                                                           | 104 ms: 1.01x slower                                                  |
| xml_etree_parse            | 144 ms                                                           | 146 ms: 1.02x slower                                                  |
| sqlglot_parse              | 1.39 ms                                                          | 1.42 ms: 1.02x slower                                                 |
| sympy_expand               | 501 ms                                                           | 512 ms: 1.02x slower                                                  |
| coroutines                 | 22.0 ms                                                          | 22.5 ms: 1.02x slower                                                 |
| sqlglot_normalize          | 120 ms                                                           | 123 ms: 1.02x slower                                                  |
| pprint_pformat             | 1.66 sec                                                         | 1.70 sec: 1.02x slower                                                |
| sqlglot_transpile          | 1.76 ms                                                          | 1.81 ms: 1.03x slower                                                 |
| docutils                   | 2.98 sec                                                         | 3.06 sec: 1.03x slower                                                |
| python_startup             | 13.2 ms                                                          | 13.6 ms: 1.03x slower                                                 |
| generators                 | 33.5 ms                                                          | 34.4 ms: 1.03x slower                                                 |
| logging_format             | 7.11 us                                                          | 7.31 us: 1.03x slower                                                 |
| json_loads                 | 25.0 us                                                          | 25.8 us: 1.03x slower                                                 |
| django_template            | 39.0 ms                                                          | 40.1 ms: 1.03x slower                                                 |
| sympy_str                  | 295 ms                                                           | 304 ms: 1.03x slower                                                  |
| dask                       | 391 ms                                                           | 403 ms: 1.03x slower                                                  |
| regex_effbot               | 3.40 ms                                                          | 3.50 ms: 1.03x slower                                                 |
| async_tree_none            | 365 ms                                                           | 377 ms: 1.03x slower                                                  |
| async_tree_cpu_io_mixed_tg | 573 ms                                                           | 592 ms: 1.03x slower                                                  |
| tornado_http               | 119 ms                                                           | 124 ms: 1.03x slower                                                  |
| gc_traversal               | 4.69 ms                                                          | 4.85 ms: 1.03x slower                                                 |
| 2to3                       | 291 ms                                                           | 302 ms: 1.04x slower                                                  |
| aiohttp                    | 1.07 ms                                                          | 1.11 ms: 1.04x slower                                                 |
| async_tree_io              | 873 ms                                                           | 906 ms: 1.04x slower                                                  |
| deepcopy                   | 377 us                                                           | 391 us: 1.04x slower                                                  |
| regex_compile              | 144 ms                                                           | 150 ms: 1.04x slower                                                  |
| dulwich_log                | 67.3 ms                                                          | 69.9 ms: 1.04x slower                                                 |
| pidigits                   | 254 ms                                                           | 264 ms: 1.04x slower                                                  |
| sympy_sum                  | 155 ms                                                           | 161 ms: 1.04x slower                                                  |
| meteor_contest             | 128 ms                                                           | 134 ms: 1.05x slower                                                  |
| pickle                     | 10.6 us                                                          | 11.1 us: 1.05x slower                                                 |
| pycparser                  | 1.22 sec                                                         | 1.28 sec: 1.05x slower                                                |
| gunicorn                   | 1.04 ms                                                          | 1.10 ms: 1.05x slower                                                 |
| pyflate                    | 482 ms                                                           | 506 ms: 1.05x slower                                                  |
| logging_simple             | 6.40 us                                                          | 6.73 us: 1.05x slower                                                 |
| sqlglot_optimize           | 59.5 ms                                                          | 62.9 ms: 1.06x slower                                                 |
| crypto_pyaes               | 73.6 ms                                                          | 77.9 ms: 1.06x slower                                                 |
| deepcopy_memo              | 37.3 us                                                          | 39.6 us: 1.06x slower                                                 |
| mdp                        | 2.46 sec                                                         | 2.63 sec: 1.07x slower                                                |
| genshi_text                | 25.9 ms                                                          | 27.7 ms: 1.07x slower                                                 |
| unpickle_pure_python       | 224 us                                                           | 241 us: 1.07x slower                                                  |
| pylint                     | 339 ms                                                           | 364 ms: 1.07x slower                                                  |
| nbody                      | 87.8 ms                                                          | 94.7 ms: 1.08x slower                                                 |
| go                         | 165 ms                                                           | 178 ms: 1.08x slower                                                  |
| genshi_xml                 | 58.1 ms                                                          | 62.7 ms: 1.08x slower                                                 |
| mypy2                      | 764 ms                                                           | 826 ms: 1.08x slower                                                  |
| sympy_integrate            | 23.2 ms                                                          | 25.1 ms: 1.08x slower                                                 |
| async_generators           | 363 ms                                                           | 398 ms: 1.10x slower                                                  |
| deltablue                  | 3.37 ms                                                          | 3.77 ms: 1.12x slower                                                 |
| fannkuch                   | 353 ms                                                           | 396 ms: 1.12x slower                                                  |
| scimark_monte_carlo        | 65.5 ms                                                          | 73.7 ms: 1.13x slower                                                 |
| pathlib                    | 17.1 ms                                                          | 19.3 ms: 1.13x slower                                                 |
| chaos                      | 59.6 ms                                                          | 67.7 ms: 1.14x slower                                                 |
| comprehensions             | 17.0 us                                                          | 19.5 us: 1.15x slower                                                 |
| raytrace                   | 260 ms                                                           | 309 ms: 1.19x slower                                                  |
| nqueens                    | 88.4 ms                                                          | 105 ms: 1.19x slower                                                  |
| hexiom                     | 6.35 ms                                                          | 7.70 ms: 1.21x slower                                                 |
| scimark_lu                 | 97.5 ms                                                          | 120 ms: 1.23x slower                                                  |
| bench_thread_pool          | 908 us                                                           | 1.12 ms: 1.23x slower                                                 |
| scimark_sor                | 119 ms                                                           | 153 ms: 1.29x slower                                                  |
| python_startup_no_site     | 8.85 ms                                                          | 11.8 ms: 1.33x slower                                                 |
| Geometric mean             | (ref)                                                            | 1.03x slower                                                          |

Benchmark hidden because not significant (8): async_tree_memoization, async_tree_none_tg, async_tree_cpu_io_mixed, pickle_list, deepcopy_reduce, scimark_fft, bench_mp_pool, async_tree_memoization_tg
Ignored benchmarks (2) of results/bm-20240605-3.13.0b2-3a83b17/bm-20240605-pythonperf2-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17.json: bpe_tokeniser, flaskblogging

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.02x
- 95% likely to have a slowdown of 1.02x
- 99% likely to have a slowdown of 1.02x

# Memory
- memory change: 1.05x