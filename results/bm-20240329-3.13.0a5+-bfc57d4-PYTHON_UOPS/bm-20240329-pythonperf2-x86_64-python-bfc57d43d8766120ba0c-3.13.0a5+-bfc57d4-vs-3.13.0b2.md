# Results vs. 3.13.0b2

- fork: python
- ref: bfc57d43d8766120ba0c
- machine: linux-x86_64
- commit hash: bfc57d4
- commit date: 2024-03-29
- overall geometric mean: 1.14x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.08x slower
- Memory change: 0.98x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240605-pythonperf2-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240329-pythonperf2-x86_64-python-bfc57d43d8766120ba0c-3.13.0a5+-bfc57d4 |
|----------------|:----------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| 2to3           | 291 ms                                                           | 325 ms: 1.11x slower                                                         |
| chameleon      | 7.40 ms                                                          | 8.14 ms: 1.10x slower                                                        |
| docutils       | 2.98 sec                                                         | 3.28 sec: 1.10x slower                                                       |
| html5lib       | 74.7 ms                                                          | 80.4 ms: 1.08x slower                                                        |
| tornado_http   | 119 ms                                                           | 129 ms: 1.08x slower                                                         |
| Geometric mean | (ref)                                                            | 1.09x slower                                                                 |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240605-pythonperf2-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240329-pythonperf2-x86_64-python-bfc57d43d8766120ba0c-3.13.0a5+-bfc57d4 |
|----------------------------|:----------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| async_tree_cpu_io_mixed    | 604 ms                                                           | 629 ms: 1.04x slower                                                         |
| async_tree_none            | 365 ms                                                           | 383 ms: 1.05x slower                                                         |
| async_tree_io_tg           | 900 ms                                                           | 944 ms: 1.05x slower                                                         |
| async_tree_none_tg         | 340 ms                                                           | 359 ms: 1.05x slower                                                         |
| async_tree_io              | 873 ms                                                           | 923 ms: 1.06x slower                                                         |
| async_tree_cpu_io_mixed_tg | 573 ms                                                           | 606 ms: 1.06x slower                                                         |
| async_tree_memoization_tg  | 421 ms                                                           | 461 ms: 1.10x slower                                                         |
| Geometric mean             | (ref)                                                            | 1.05x slower                                                                 |

Benchmark hidden because not significant (1): async_tree_memoization

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240605-pythonperf2-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240329-pythonperf2-x86_64-python-bfc57d43d8766120ba0c-3.13.0a5+-bfc57d4 |
|----------------|:----------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| pidigits       | 254 ms                                                           | 265 ms: 1.04x slower                                                         |
| float          | 80.2 ms                                                          | 102 ms: 1.27x slower                                                         |
| nbody          | 87.8 ms                                                          | 129 ms: 1.47x slower                                                         |
| Geometric mean | (ref)                                                            | 1.25x slower                                                                 |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240605-pythonperf2-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240329-pythonperf2-x86_64-python-bfc57d43d8766120ba0c-3.13.0a5+-bfc57d4 |
|----------------|:----------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| regex_dna      | 249 ms                                                           | 242 ms: 1.03x faster                                                         |
| regex_v8       | 26.0 ms                                                          | 25.9 ms: 1.00x faster                                                        |
| regex_effbot   | 3.40 ms                                                          | 3.47 ms: 1.02x slower                                                        |
| regex_compile  | 144 ms                                                           | 209 ms: 1.45x slower                                                         |
| Geometric mean | (ref)                                                            | 1.09x slower                                                                 |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240605-pythonperf2-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240329-pythonperf2-x86_64-python-bfc57d43d8766120ba0c-3.13.0a5+-bfc57d4 |
|----------------------|:----------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| unpickle             | 15.7 us                                                          | 14.8 us: 1.06x faster                                                        |
| unpickle_list        | 4.70 us                                                          | 4.59 us: 1.02x faster                                                        |
| json_dumps           | 10.8 ms                                                          | 10.9 ms: 1.01x slower                                                        |
| xml_etree_parse      | 144 ms                                                           | 146 ms: 1.02x slower                                                         |
| pickle               | 10.6 us                                                          | 10.9 us: 1.03x slower                                                        |
| json_loads           | 25.0 us                                                          | 25.8 us: 1.03x slower                                                        |
| xml_etree_process    | 59.7 ms                                                          | 63.4 ms: 1.06x slower                                                        |
| pickle_pure_python   | 307 us                                                           | 328 us: 1.07x slower                                                         |
| pickle_dict          | 32.8 us                                                          | 35.2 us: 1.07x slower                                                        |
| xml_etree_generate   | 85.7 ms                                                          | 92.4 ms: 1.08x slower                                                        |
| xml_etree_iterparse  | 103 ms                                                           | 113 ms: 1.11x slower                                                         |
| tomli_loads          | 2.40 sec                                                         | 2.98 sec: 1.24x slower                                                       |
| unpickle_pure_python | 224 us                                                           | 319 us: 1.42x slower                                                         |
| Geometric mean       | (ref)                                                            | 1.07x slower                                                                 |

Benchmark hidden because not significant (1): pickle_list

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240605-pythonperf2-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240329-pythonperf2-x86_64-python-bfc57d43d8766120ba0c-3.13.0a5+-bfc57d4 |
|------------------------|:----------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| python_startup         | 13.2 ms                                                          | 12.9 ms: 1.02x faster                                                        |
| python_startup_no_site | 8.85 ms                                                          | 11.2 ms: 1.26x slower                                                        |
| Geometric mean         | (ref)                                                            | 1.11x slower                                                                 |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240605-pythonperf2-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240329-pythonperf2-x86_64-python-bfc57d43d8766120ba0c-3.13.0a5+-bfc57d4 |
|-----------------|:----------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| genshi_text     | 25.9 ms                                                          | 27.0 ms: 1.04x slower                                                        |
| genshi_xml      | 58.1 ms                                                          | 61.9 ms: 1.07x slower                                                        |
| django_template | 39.0 ms                                                          | 42.3 ms: 1.08x slower                                                        |
| mako            | 10.4 ms                                                          | 14.4 ms: 1.39x slower                                                        |
| Geometric mean  | (ref)                                                            | 1.14x slower                                                                 |

All benchmarks:
===============

| Benchmark                  | bm-20240605-pythonperf2-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240329-pythonperf2-x86_64-python-bfc57d43d8766120ba0c-3.13.0a5+-bfc57d4 |
|----------------------------|:----------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| typing_runtime_protocols   | 171 us                                                           | 128 us: 1.33x faster                                                         |
| create_gc_cycles           | 2.00 ms                                                          | 1.84 ms: 1.09x faster                                                        |
| gc_traversal               | 4.69 ms                                                          | 4.39 ms: 1.07x faster                                                        |
| unpickle                   | 15.7 us                                                          | 14.8 us: 1.06x faster                                                        |
| regex_dna                  | 249 ms                                                           | 242 ms: 1.03x faster                                                         |
| unpickle_list              | 4.70 us                                                          | 4.59 us: 1.02x faster                                                        |
| python_startup             | 13.2 ms                                                          | 12.9 ms: 1.02x faster                                                        |
| asyncio_websockets         | 395 ms                                                           | 390 ms: 1.01x faster                                                         |
| regex_v8                   | 26.0 ms                                                          | 25.9 ms: 1.00x faster                                                        |
| coverage                   | 83.5 ms                                                          | 83.9 ms: 1.01x slower                                                        |
| json_dumps                 | 10.8 ms                                                          | 10.9 ms: 1.01x slower                                                        |
| asyncio_tcp_ssl            | 1.58 sec                                                         | 1.60 sec: 1.01x slower                                                       |
| telco                      | 8.40 ms                                                          | 8.54 ms: 1.02x slower                                                        |
| xml_etree_parse            | 144 ms                                                           | 146 ms: 1.02x slower                                                         |
| coroutines                 | 22.0 ms                                                          | 22.5 ms: 1.02x slower                                                        |
| regex_effbot               | 3.40 ms                                                          | 3.47 ms: 1.02x slower                                                        |
| thrift                     | 880 us                                                           | 900 us: 1.02x slower                                                         |
| pickle                     | 10.6 us                                                          | 10.9 us: 1.03x slower                                                        |
| json_loads                 | 25.0 us                                                          | 25.8 us: 1.03x slower                                                        |
| pylint                     | 339 ms                                                           | 351 ms: 1.03x slower                                                         |
| async_tree_cpu_io_mixed    | 604 ms                                                           | 629 ms: 1.04x slower                                                         |
| sqlite_synth               | 2.80 us                                                          | 2.91 us: 1.04x slower                                                        |
| deepcopy_reduce            | 3.39 us                                                          | 3.53 us: 1.04x slower                                                        |
| generators                 | 33.5 ms                                                          | 34.9 ms: 1.04x slower                                                        |
| genshi_text                | 25.9 ms                                                          | 27.0 ms: 1.04x slower                                                        |
| pidigits                   | 254 ms                                                           | 265 ms: 1.04x slower                                                         |
| json                       | 5.35 ms                                                          | 5.60 ms: 1.05x slower                                                        |
| async_tree_none            | 365 ms                                                           | 383 ms: 1.05x slower                                                         |
| async_tree_io_tg           | 900 ms                                                           | 944 ms: 1.05x slower                                                         |
| async_tree_none_tg         | 340 ms                                                           | 359 ms: 1.05x slower                                                         |
| async_tree_io              | 873 ms                                                           | 923 ms: 1.06x slower                                                         |
| async_tree_cpu_io_mixed_tg | 573 ms                                                           | 606 ms: 1.06x slower                                                         |
| gunicorn                   | 1.04 ms                                                          | 1.11 ms: 1.06x slower                                                        |
| xml_etree_process          | 59.7 ms                                                          | 63.4 ms: 1.06x slower                                                        |
| bench_mp_pool              | 4.91 ms                                                          | 5.22 ms: 1.06x slower                                                        |
| genshi_xml                 | 58.1 ms                                                          | 61.9 ms: 1.07x slower                                                        |
| pickle_pure_python         | 307 us                                                           | 328 us: 1.07x slower                                                         |
| logging_format             | 7.11 us                                                          | 7.60 us: 1.07x slower                                                        |
| dask                       | 391 ms                                                           | 418 ms: 1.07x slower                                                         |
| aiohttp                    | 1.07 ms                                                          | 1.15 ms: 1.07x slower                                                        |
| pickle_dict                | 32.8 us                                                          | 35.2 us: 1.07x slower                                                        |
| deepcopy                   | 377 us                                                           | 405 us: 1.07x slower                                                         |
| html5lib                   | 74.7 ms                                                          | 80.4 ms: 1.08x slower                                                        |
| xml_etree_generate         | 85.7 ms                                                          | 92.4 ms: 1.08x slower                                                        |
| tornado_http               | 119 ms                                                           | 129 ms: 1.08x slower                                                         |
| logging_simple             | 6.40 us                                                          | 6.93 us: 1.08x slower                                                        |
| logging_silent             | 96.3 ns                                                          | 104 ns: 1.08x slower                                                         |
| django_template            | 39.0 ms                                                          | 42.3 ms: 1.08x slower                                                        |
| sqlglot_normalize          | 120 ms                                                           | 131 ms: 1.09x slower                                                         |
| async_tree_memoization_tg  | 421 ms                                                           | 461 ms: 1.10x slower                                                         |
| chameleon                  | 7.40 ms                                                          | 8.14 ms: 1.10x slower                                                        |
| mdp                        | 2.46 sec                                                         | 2.71 sec: 1.10x slower                                                       |
| docutils                   | 2.98 sec                                                         | 3.28 sec: 1.10x slower                                                       |
| async_generators           | 363 ms                                                           | 400 ms: 1.10x slower                                                         |
| xml_etree_iterparse        | 103 ms                                                           | 113 ms: 1.11x slower                                                         |
| richards_super             | 61.2 ms                                                          | 68.0 ms: 1.11x slower                                                        |
| 2to3                       | 291 ms                                                           | 325 ms: 1.11x slower                                                         |
| meteor_contest             | 128 ms                                                           | 143 ms: 1.12x slower                                                         |
| mypy2                      | 764 ms                                                           | 865 ms: 1.13x slower                                                         |
| richards                   | 53.4 ms                                                          | 61.1 ms: 1.14x slower                                                        |
| dulwich_log                | 67.3 ms                                                          | 77.3 ms: 1.15x slower                                                        |
| sqlglot_optimize           | 59.5 ms                                                          | 68.5 ms: 1.15x slower                                                        |
| sqlglot_transpile          | 1.76 ms                                                          | 2.04 ms: 1.15x slower                                                        |
| sqlglot_parse              | 1.39 ms                                                          | 1.61 ms: 1.16x slower                                                        |
| sympy_integrate            | 23.2 ms                                                          | 27.0 ms: 1.17x slower                                                        |
| sympy_sum                  | 155 ms                                                           | 181 ms: 1.17x slower                                                         |
| sympy_expand               | 501 ms                                                           | 587 ms: 1.17x slower                                                         |
| sympy_str                  | 295 ms                                                           | 350 ms: 1.19x slower                                                         |
| pycparser                  | 1.22 sec                                                         | 1.47 sec: 1.20x slower                                                       |
| deepcopy_memo              | 37.3 us                                                          | 45.4 us: 1.22x slower                                                        |
| pathlib                    | 17.1 ms                                                          | 21.0 ms: 1.22x slower                                                        |
| deltablue                  | 3.37 ms                                                          | 4.15 ms: 1.23x slower                                                        |
| pprint_safe_repr           | 818 ms                                                           | 1.01 sec: 1.24x slower                                                       |
| go                         | 165 ms                                                           | 204 ms: 1.24x slower                                                         |
| tomli_loads                | 2.40 sec                                                         | 2.98 sec: 1.24x slower                                                       |
| pprint_pformat             | 1.66 sec                                                         | 2.06 sec: 1.24x slower                                                       |
| bench_thread_pool          | 908 us                                                           | 1.14 ms: 1.25x slower                                                        |
| crypto_pyaes               | 73.6 ms                                                          | 92.5 ms: 1.26x slower                                                        |
| python_startup_no_site     | 8.85 ms                                                          | 11.2 ms: 1.26x slower                                                        |
| float                      | 80.2 ms                                                          | 102 ms: 1.27x slower                                                         |
| chaos                      | 59.6 ms                                                          | 77.7 ms: 1.30x slower                                                        |
| raytrace                   | 260 ms                                                           | 352 ms: 1.35x slower                                                         |
| pyflate                    | 482 ms                                                           | 666 ms: 1.38x slower                                                         |
| nqueens                    | 88.4 ms                                                          | 122 ms: 1.38x slower                                                         |
| mako                       | 10.4 ms                                                          | 14.4 ms: 1.39x slower                                                        |
| scimark_sor                | 119 ms                                                           | 167 ms: 1.40x slower                                                         |
| unpickle_pure_python       | 224 us                                                           | 319 us: 1.42x slower                                                         |
| scimark_fft                | 312 ms                                                           | 446 ms: 1.43x slower                                                         |
| fannkuch                   | 353 ms                                                           | 507 ms: 1.44x slower                                                         |
| regex_compile              | 144 ms                                                           | 209 ms: 1.45x slower                                                         |
| nbody                      | 87.8 ms                                                          | 129 ms: 1.47x slower                                                         |
| scimark_lu                 | 97.5 ms                                                          | 152 ms: 1.56x slower                                                         |
| scimark_monte_carlo        | 65.5 ms                                                          | 102 ms: 1.56x slower                                                         |
| comprehensions             | 17.0 us                                                          | 26.8 us: 1.58x slower                                                        |
| scimark_sparse_mat_mult    | 4.28 ms                                                          | 6.79 ms: 1.59x slower                                                        |
| spectral_norm              | 97.3 ms                                                          | 158 ms: 1.62x slower                                                         |
| hexiom                     | 6.35 ms                                                          | 11.0 ms: 1.73x slower                                                        |
| Geometric mean             | (ref)                                                            | 1.14x slower                                                                 |

Benchmark hidden because not significant (3): asyncio_tcp, pickle_list, async_tree_memoization
Ignored benchmarks (2) of results/bm-20240605-3.13.0b2-3a83b17/bm-20240605-pythonperf2-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17.json: bpe_tokeniser, flaskblogging
Ignored benchmarks (1) of results/bm-20240329-3.13.0a5+-bfc57d4-PYTHON_UOPS/bm-20240329-pythonperf2-x86_64-python-bfc57d43d8766120ba0c-3.13.0a5+-bfc57d4.json: unpack_sequence

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.10x
- 95% likely to have a slowdown of 1.09x
- 99% likely to have a slowdown of 1.08x

# Memory
- memory change: 0.98x