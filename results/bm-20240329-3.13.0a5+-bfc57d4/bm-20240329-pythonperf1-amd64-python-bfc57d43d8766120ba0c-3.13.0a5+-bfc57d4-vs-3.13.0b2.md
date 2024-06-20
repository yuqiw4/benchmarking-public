# Results vs. 3.13.0b2

- fork: python
- ref: bfc57d43d8766120ba0c
- machine: windows-amd64
- commit hash: bfc57d4
- commit date: 2024-03-29
- overall geometric mean: 1.00x faster
- HPT reliability: 87.49%
- HPT 99th percentile: 1.00x slower
- Memory change: unknown

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240605-pythonperf1-amd64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240329-pythonperf1-amd64-python-bfc57d43d8766120ba0c-3.13.0a5+-bfc57d4 |
|----------------|:---------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| 2to3           | 207 ms                                                          | 208 ms: 1.01x slower                                                        |
| chameleon      | 4.80 ms                                                         | 4.72 ms: 1.02x faster                                                       |
| docutils       | 1.63 sec                                                        | 1.61 sec: 1.01x faster                                                      |
| html5lib       | 35.0 ms                                                         | 35.7 ms: 1.02x slower                                                       |
| tornado_http   | 81.8 ms                                                         | 83.7 ms: 1.02x slower                                                       |
| Geometric mean | (ref)                                                           | 1.00x slower                                                                |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                 | bm-20240605-pythonperf1-amd64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240329-pythonperf1-amd64-python-bfc57d43d8766120ba0c-3.13.0a5+-bfc57d4 |
|---------------------------|:---------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| async_tree_cpu_io_mixed   | 389 ms                                                          | 380 ms: 1.02x faster                                                        |
| async_tree_io_tg          | 605 ms                                                          | 616 ms: 1.02x slower                                                        |
| async_tree_memoization_tg | 258 ms                                                          | 270 ms: 1.04x slower                                                        |
| Geometric mean            | (ref)                                                           | 1.01x slower                                                                |

Benchmark hidden because not significant (5): async_tree_io, async_tree_cpu_io_mixed_tg, async_tree_none, async_tree_none_tg, async_tree_memoization

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240605-pythonperf1-amd64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240329-pythonperf1-amd64-python-bfc57d43d8766120ba0c-3.13.0a5+-bfc57d4 |
|----------------|:---------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| pidigits       | 150 ms                                                          | 146 ms: 1.02x faster                                                        |
| float          | 49.7 ms                                                         | 50.4 ms: 1.01x slower                                                       |
| Geometric mean | (ref)                                                           | 1.00x faster                                                                |

Benchmark hidden because not significant (1): nbody

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240605-pythonperf1-amd64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240329-pythonperf1-amd64-python-bfc57d43d8766120ba0c-3.13.0a5+-bfc57d4 |
|----------------|:---------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| regex_v8       | 15.8 ms                                                         | 14.7 ms: 1.07x faster                                                       |
| regex_compile  | 78.0 ms                                                         | 75.2 ms: 1.04x faster                                                       |
| regex_dna      | 119 ms                                                          | 120 ms: 1.01x slower                                                        |
| Geometric mean | (ref)                                                           | 1.03x faster                                                                |

Benchmark hidden because not significant (1): regex_effbot

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240605-pythonperf1-amd64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240329-pythonperf1-amd64-python-bfc57d43d8766120ba0c-3.13.0a5+-bfc57d4 |
|----------------------|:---------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| json_loads           | 14.2 us                                                         | 13.8 us: 1.03x faster                                                       |
| pickle               | 7.11 us                                                         | 6.96 us: 1.02x faster                                                       |
| pickle_list          | 2.90 us                                                         | 2.84 us: 1.02x faster                                                       |
| xml_etree_generate   | 53.2 ms                                                         | 52.3 ms: 1.02x faster                                                       |
| json_dumps           | 5.61 ms                                                         | 5.58 ms: 1.01x faster                                                       |
| pickle_dict          | 18.1 us                                                         | 18.0 us: 1.01x faster                                                       |
| pickle_pure_python   | 175 us                                                          | 175 us: 1.00x faster                                                        |
| unpickle_pure_python | 122 us                                                          | 127 us: 1.04x slower                                                        |
| tomli_loads          | 1.35 sec                                                        | 1.41 sec: 1.04x slower                                                      |
| Geometric mean       | (ref)                                                           | 1.00x faster                                                                |

Benchmark hidden because not significant (5): unpickle, xml_etree_iterparse, xml_etree_process, unpickle_list, xml_etree_parse

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240605-pythonperf1-amd64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240329-pythonperf1-amd64-python-bfc57d43d8766120ba0c-3.13.0a5+-bfc57d4 |
|------------------------|:---------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| python_startup         | 20.3 ms                                                         | 20.0 ms: 1.02x faster                                                       |
| python_startup_no_site | 16.2 ms                                                         | 18.5 ms: 1.14x slower                                                       |
| Geometric mean         | (ref)                                                           | 1.06x slower                                                                |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240605-pythonperf1-amd64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240329-pythonperf1-amd64-python-bfc57d43d8766120ba0c-3.13.0a5+-bfc57d4 |
|-----------------|:---------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| mako            | 6.36 ms                                                         | 6.26 ms: 1.02x faster                                                       |
| django_template | 21.7 ms                                                         | 21.8 ms: 1.01x slower                                                       |
| genshi_xml      | 31.6 ms                                                         | 33.7 ms: 1.07x slower                                                       |
| genshi_text     | 14.4 ms                                                         | 15.8 ms: 1.10x slower                                                       |
| Geometric mean  | (ref)                                                           | 1.04x slower                                                                |

All benchmarks:
===============

| Benchmark                 | bm-20240605-pythonperf1-amd64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240329-pythonperf1-amd64-python-bfc57d43d8766120ba0c-3.13.0a5+-bfc57d4 |
|---------------------------|:---------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| typing_runtime_protocols  | 101 us                                                          | 72.1 us: 1.40x faster                                                       |
| pycparser                 | 754 ms                                                          | 675 ms: 1.12x faster                                                        |
| scimark_lu                | 56.6 ms                                                         | 50.8 ms: 1.11x faster                                                       |
| pylint                    | 205 ms                                                          | 187 ms: 1.09x faster                                                        |
| json                      | 3.19 ms                                                         | 2.92 ms: 1.09x faster                                                       |
| spectral_norm             | 63.7 ms                                                         | 58.4 ms: 1.09x faster                                                       |
| scimark_sparse_mat_mult   | 2.50 ms                                                         | 2.29 ms: 1.09x faster                                                       |
| regex_v8                  | 15.8 ms                                                         | 14.7 ms: 1.07x faster                                                       |
| crypto_pyaes              | 45.5 ms                                                         | 43.1 ms: 1.05x faster                                                       |
| create_gc_cycles          | 888 us                                                          | 847 us: 1.05x faster                                                        |
| regex_compile             | 78.0 ms                                                         | 75.2 ms: 1.04x faster                                                       |
| deepcopy_memo             | 22.1 us                                                         | 21.3 us: 1.04x faster                                                       |
| scimark_sor               | 75.3 ms                                                         | 72.7 ms: 1.04x faster                                                       |
| scimark_fft               | 171 ms                                                          | 165 ms: 1.03x faster                                                        |
| chaos                     | 38.4 ms                                                         | 37.1 ms: 1.03x faster                                                       |
| json_loads                | 14.2 us                                                         | 13.8 us: 1.03x faster                                                       |
| deepcopy_reduce           | 1.99 us                                                         | 1.94 us: 1.03x faster                                                       |
| async_tree_cpu_io_mixed   | 389 ms                                                          | 380 ms: 1.02x faster                                                        |
| pidigits                  | 150 ms                                                          | 146 ms: 1.02x faster                                                        |
| raytrace                  | 162 ms                                                          | 159 ms: 1.02x faster                                                        |
| pickle                    | 7.11 us                                                         | 6.96 us: 1.02x faster                                                       |
| pickle_list               | 2.90 us                                                         | 2.84 us: 1.02x faster                                                       |
| chameleon                 | 4.80 ms                                                         | 4.72 ms: 1.02x faster                                                       |
| sympy_sum                 | 84.4 ms                                                         | 82.9 ms: 1.02x faster                                                       |
| xml_etree_generate        | 53.2 ms                                                         | 52.3 ms: 1.02x faster                                                       |
| deepcopy                  | 220 us                                                          | 216 us: 1.02x faster                                                        |
| mako                      | 6.36 ms                                                         | 6.26 ms: 1.02x faster                                                       |
| bench_mp_pool             | 64.8 ms                                                         | 63.8 ms: 1.02x faster                                                       |
| python_startup            | 20.3 ms                                                         | 20.0 ms: 1.02x faster                                                       |
| hexiom                    | 3.72 ms                                                         | 3.67 ms: 1.02x faster                                                       |
| gc_traversal              | 1.55 ms                                                         | 1.53 ms: 1.01x faster                                                       |
| scimark_monte_carlo       | 39.1 ms                                                         | 38.6 ms: 1.01x faster                                                       |
| docutils                  | 1.63 sec                                                        | 1.61 sec: 1.01x faster                                                      |
| json_dumps                | 5.61 ms                                                         | 5.58 ms: 1.01x faster                                                       |
| pickle_dict               | 18.1 us                                                         | 18.0 us: 1.01x faster                                                       |
| sympy_str                 | 159 ms                                                          | 158 ms: 1.01x faster                                                        |
| richards_super            | 30.2 ms                                                         | 30.0 ms: 1.01x faster                                                       |
| sqlglot_parse             | 748 us                                                          | 745 us: 1.00x faster                                                        |
| pickle_pure_python        | 175 us                                                          | 175 us: 1.00x faster                                                        |
| fannkuch                  | 243 ms                                                          | 243 ms: 1.00x faster                                                        |
| sqlite_synth              | 1.60 us                                                         | 1.59 us: 1.00x faster                                                       |
| pprint_pformat            | 966 ms                                                          | 970 ms: 1.00x slower                                                        |
| pprint_safe_repr          | 474 ms                                                          | 476 ms: 1.00x slower                                                        |
| pyflate                   | 279 ms                                                          | 280 ms: 1.01x slower                                                        |
| django_template           | 21.7 ms                                                         | 21.8 ms: 1.01x slower                                                       |
| regex_dna                 | 119 ms                                                          | 120 ms: 1.01x slower                                                        |
| 2to3                      | 207 ms                                                          | 208 ms: 1.01x slower                                                        |
| meteor_contest            | 69.9 ms                                                         | 70.5 ms: 1.01x slower                                                       |
| nqueens                   | 56.7 ms                                                         | 57.3 ms: 1.01x slower                                                       |
| sqlglot_optimize          | 32.7 ms                                                         | 33.1 ms: 1.01x slower                                                       |
| float                     | 49.7 ms                                                         | 50.4 ms: 1.01x slower                                                       |
| sqlglot_normalize         | 173 ms                                                          | 175 ms: 1.01x slower                                                        |
| async_tree_io_tg          | 605 ms                                                          | 616 ms: 1.02x slower                                                        |
| html5lib                  | 35.0 ms                                                         | 35.7 ms: 1.02x slower                                                       |
| go                        | 82.1 ms                                                         | 83.6 ms: 1.02x slower                                                       |
| telco                     | 4.67 ms                                                         | 4.77 ms: 1.02x slower                                                       |
| tornado_http              | 81.8 ms                                                         | 83.7 ms: 1.02x slower                                                       |
| pathlib                   | 75.9 ms                                                         | 78.0 ms: 1.03x slower                                                       |
| logging_simple            | 5.78 us                                                         | 5.95 us: 1.03x slower                                                       |
| logging_format            | 6.22 us                                                         | 6.44 us: 1.03x slower                                                       |
| mypy2                     | 418 ms                                                          | 433 ms: 1.04x slower                                                        |
| unpickle_pure_python      | 122 us                                                          | 127 us: 1.04x slower                                                        |
| tomli_loads               | 1.35 sec                                                        | 1.41 sec: 1.04x slower                                                      |
| logging_silent            | 52.9 ns                                                         | 55.1 ns: 1.04x slower                                                       |
| async_tree_memoization_tg | 258 ms                                                          | 270 ms: 1.04x slower                                                        |
| mdp                       | 1.31 sec                                                        | 1.37 sec: 1.05x slower                                                      |
| dulwich_log               | 38.0 ms                                                         | 40.0 ms: 1.05x slower                                                       |
| deltablue                 | 1.88 ms                                                         | 1.98 ms: 1.05x slower                                                       |
| bench_thread_pool         | 768 us                                                          | 814 us: 1.06x slower                                                        |
| genshi_xml                | 31.6 ms                                                         | 33.7 ms: 1.07x slower                                                       |
| coroutines                | 12.8 ms                                                         | 13.7 ms: 1.07x slower                                                       |
| async_generators          | 223 ms                                                          | 240 ms: 1.07x slower                                                        |
| genshi_text               | 14.4 ms                                                         | 15.8 ms: 1.10x slower                                                       |
| coverage                  | 42.1 ms                                                         | 46.3 ms: 1.10x slower                                                       |
| python_startup_no_site    | 16.2 ms                                                         | 18.5 ms: 1.14x slower                                                       |
| generators                | 19.6 ms                                                         | 22.6 ms: 1.15x slower                                                       |
| asyncio_tcp_ssl           | 1.48 sec                                                        | 1.75 sec: 1.18x slower                                                      |
| Geometric mean            | (ref)                                                           | 1.00x faster                                                                |

Benchmark hidden because not significant (20): async_tree_io, asyncio_tcp, richards, sympy_integrate, unpickle, xml_etree_iterparse, regex_effbot, xml_etree_process, thrift, async_tree_cpu_io_mixed_tg, comprehensions, async_tree_none, unpickle_list, sqlglot_transpile, xml_etree_parse, nbody, aiohttp, sympy_expand, async_tree_none_tg, async_tree_memoization
Ignored benchmarks (1) of results/bm-20240605-3.13.0b2-3a83b17/bm-20240605-pythonperf1-amd64-python-v3.13.0b2-3.13.0b2-3a83b17.json: flaskblogging
Ignored benchmarks (1) of results/bm-20240329-3.13.0a5+-bfc57d4/bm-20240329-pythonperf1-amd64-python-bfc57d43d8766120ba0c-3.13.0a5+-bfc57d4.json: unpack_sequence

# HPT report

- Reliability score: 87.49% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: unknown