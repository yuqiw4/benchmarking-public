# Results vs. 3.13.0b2

- fork: python
- ref: 15fbd53ba96be4b6a5ab
- machine: windows-x86
- commit hash: 15fbd53
- commit date: 2024-04-20
- overall geometric mean: 1.04x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.01x slower
- Memory change: unknown

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240605-pythonperf1_win32-x86-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240420-pythonperf1_win32-x86-python-15fbd53ba96be4b6a5ab-3.13.0a6+-15fbd53 |
|----------------|:-------------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| 2to3           | 233 ms                                                              | 242 ms: 1.04x slower                                                            |
| chameleon      | 5.71 ms                                                             | 5.74 ms: 1.01x slower                                                           |
| docutils       | 1.81 sec                                                            | 1.90 sec: 1.05x slower                                                          |
| html5lib       | 45.4 ms                                                             | 44.8 ms: 1.01x faster                                                           |
| tornado_http   | 94.3 ms                                                             | 96.6 ms: 1.02x slower                                                           |
| Geometric mean | (ref)                                                               | 1.02x slower                                                                    |

Benchmarks with tag 'asyncio':
==============================

| Benchmark          | bm-20240605-pythonperf1_win32-x86-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240420-pythonperf1_win32-x86-python-15fbd53ba96be4b6a5ab-3.13.0a6+-15fbd53 |
|--------------------|:-------------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| async_tree_none    | 228 ms                                                              | 231 ms: 1.01x slower                                                            |
| async_tree_none_tg | 203 ms                                                              | 210 ms: 1.03x slower                                                            |
| Geometric mean     | (ref)                                                               | 1.01x slower                                                                    |

Benchmark hidden because not significant (6): async_tree_cpu_io_mixed_tg, async_tree_cpu_io_mixed, async_tree_io_tg, async_tree_io, async_tree_memoization, async_tree_memoization_tg

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240605-pythonperf1_win32-x86-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240420-pythonperf1_win32-x86-python-15fbd53ba96be4b6a5ab-3.13.0a6+-15fbd53 |
|----------------|:-------------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| pidigits       | 199 ms                                                              | 200 ms: 1.01x slower                                                            |
| nbody          | 76.9 ms                                                             | 79.1 ms: 1.03x slower                                                           |
| float          | 52.4 ms                                                             | 55.1 ms: 1.05x slower                                                           |
| Geometric mean | (ref)                                                               | 1.03x slower                                                                    |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240605-pythonperf1_win32-x86-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240420-pythonperf1_win32-x86-python-15fbd53ba96be4b6a5ab-3.13.0a6+-15fbd53 |
|----------------|:-------------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| regex_effbot   | 1.88 ms                                                             | 1.90 ms: 1.01x slower                                                           |
| regex_dna      | 118 ms                                                              | 120 ms: 1.02x slower                                                            |
| regex_v8       | 15.7 ms                                                             | 16.1 ms: 1.02x slower                                                           |
| regex_compile  | 99.9 ms                                                             | 119 ms: 1.19x slower                                                            |
| Geometric mean | (ref)                                                               | 1.06x slower                                                                    |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240605-pythonperf1_win32-x86-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240420-pythonperf1_win32-x86-python-15fbd53ba96be4b6a5ab-3.13.0a6+-15fbd53 |
|----------------------|:-------------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| unpickle_list        | 2.93 us                                                             | 2.70 us: 1.09x faster                                                           |
| pickle_list          | 3.57 us                                                             | 3.33 us: 1.07x faster                                                           |
| pickle               | 8.07 us                                                             | 7.76 us: 1.04x faster                                                           |
| pickle_dict          | 20.8 us                                                             | 20.3 us: 1.02x faster                                                           |
| tomli_loads          | 1.65 sec                                                            | 1.63 sec: 1.01x faster                                                          |
| json_loads           | 20.5 us                                                             | 20.3 us: 1.01x faster                                                           |
| xml_etree_generate   | 59.6 ms                                                             | 60.1 ms: 1.01x slower                                                           |
| unpickle             | 9.79 us                                                             | 9.94 us: 1.02x slower                                                           |
| xml_etree_parse      | 104 ms                                                              | 106 ms: 1.02x slower                                                            |
| pickle_pure_python   | 213 us                                                              | 218 us: 1.02x slower                                                            |
| json_dumps           | 6.84 ms                                                             | 7.02 ms: 1.03x slower                                                           |
| xml_etree_process    | 42.1 ms                                                             | 43.4 ms: 1.03x slower                                                           |
| xml_etree_iterparse  | 64.2 ms                                                             | 67.1 ms: 1.04x slower                                                           |
| unpickle_pure_python | 147 us                                                              | 164 us: 1.12x slower                                                            |
| Geometric mean       | (ref)                                                               | 1.00x slower                                                                    |

Benchmarks with tag 'startup':
==============================

| Benchmark      | bm-20240605-pythonperf1_win32-x86-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240420-pythonperf1_win32-x86-python-15fbd53ba96be4b6a5ab-3.13.0a6+-15fbd53 |
|----------------|:-------------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| python_startup | 22.2 ms                                                             | 21.9 ms: 1.02x faster                                                           |
| Geometric mean | (ref)                                                               | 1.01x faster                                                                    |

Benchmark hidden because not significant (1): python_startup_no_site

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240605-pythonperf1_win32-x86-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240420-pythonperf1_win32-x86-python-15fbd53ba96be4b6a5ab-3.13.0a6+-15fbd53 |
|-----------------|:-------------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| mako            | 6.94 ms                                                             | 7.01 ms: 1.01x slower                                                           |
| genshi_text     | 20.1 ms                                                             | 20.9 ms: 1.04x slower                                                           |
| genshi_xml      | 44.3 ms                                                             | 46.8 ms: 1.06x slower                                                           |
| django_template | 30.1 ms                                                             | 31.9 ms: 1.06x slower                                                           |
| Geometric mean  | (ref)                                                               | 1.04x slower                                                                    |

All benchmarks:
===============

| Benchmark                | bm-20240605-pythonperf1_win32-x86-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240420-pythonperf1_win32-x86-python-15fbd53ba96be4b6a5ab-3.13.0a6+-15fbd53 |
|--------------------------|:-------------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| typing_runtime_protocols | 136 us                                                              | 92.9 us: 1.46x faster                                                           |
| unpickle_list            | 2.93 us                                                             | 2.70 us: 1.09x faster                                                           |
| pickle_list              | 3.57 us                                                             | 3.33 us: 1.07x faster                                                           |
| asyncio_tcp              | 662 ms                                                              | 627 ms: 1.06x faster                                                            |
| richards                 | 31.2 ms                                                             | 29.7 ms: 1.05x faster                                                           |
| richards_super           | 35.5 ms                                                             | 33.7 ms: 1.05x faster                                                           |
| pickle                   | 8.07 us                                                             | 7.76 us: 1.04x faster                                                           |
| create_gc_cycles         | 756 us                                                              | 731 us: 1.03x faster                                                            |
| pickle_dict              | 20.8 us                                                             | 20.3 us: 1.02x faster                                                           |
| sqlite_synth             | 1.96 us                                                             | 1.93 us: 1.02x faster                                                           |
| coroutines               | 15.5 ms                                                             | 15.2 ms: 1.02x faster                                                           |
| python_startup           | 22.2 ms                                                             | 21.9 ms: 1.02x faster                                                           |
| html5lib                 | 45.4 ms                                                             | 44.8 ms: 1.01x faster                                                           |
| tomli_loads              | 1.65 sec                                                            | 1.63 sec: 1.01x faster                                                          |
| json_loads               | 20.5 us                                                             | 20.3 us: 1.01x faster                                                           |
| deepcopy_reduce          | 2.59 us                                                             | 2.57 us: 1.01x faster                                                           |
| sqlglot_parse            | 964 us                                                              | 955 us: 1.01x faster                                                            |
| asyncio_tcp_ssl          | 16.9 sec                                                            | 16.7 sec: 1.01x faster                                                          |
| pprint_safe_repr         | 607 ms                                                              | 603 ms: 1.01x faster                                                            |
| pprint_pformat           | 1.24 sec                                                            | 1.23 sec: 1.01x faster                                                          |
| chameleon                | 5.71 ms                                                             | 5.74 ms: 1.01x slower                                                           |
| sqlglot_transpile        | 1.19 ms                                                             | 1.20 ms: 1.01x slower                                                           |
| deepcopy                 | 280 us                                                              | 281 us: 1.01x slower                                                            |
| pathlib                  | 83.9 ms                                                             | 84.4 ms: 1.01x slower                                                           |
| telco                    | 6.03 ms                                                             | 6.08 ms: 1.01x slower                                                           |
| xml_etree_generate       | 59.6 ms                                                             | 60.1 ms: 1.01x slower                                                           |
| json                     | 4.10 ms                                                             | 4.13 ms: 1.01x slower                                                           |
| regex_effbot             | 1.88 ms                                                             | 1.90 ms: 1.01x slower                                                           |
| mako                     | 6.94 ms                                                             | 7.01 ms: 1.01x slower                                                           |
| pidigits                 | 199 ms                                                              | 200 ms: 1.01x slower                                                            |
| async_tree_none          | 228 ms                                                              | 231 ms: 1.01x slower                                                            |
| unpickle                 | 9.79 us                                                             | 9.94 us: 1.02x slower                                                           |
| bench_thread_pool        | 985 us                                                              | 1.00 ms: 1.02x slower                                                           |
| regex_dna                | 118 ms                                                              | 120 ms: 1.02x slower                                                            |
| xml_etree_parse          | 104 ms                                                              | 106 ms: 1.02x slower                                                            |
| regex_v8                 | 15.7 ms                                                             | 16.1 ms: 1.02x slower                                                           |
| pickle_pure_python       | 213 us                                                              | 218 us: 1.02x slower                                                            |
| tornado_http             | 94.3 ms                                                             | 96.6 ms: 1.02x slower                                                           |
| json_dumps               | 6.84 ms                                                             | 7.02 ms: 1.03x slower                                                           |
| nbody                    | 76.9 ms                                                             | 79.1 ms: 1.03x slower                                                           |
| xml_etree_process        | 42.1 ms                                                             | 43.4 ms: 1.03x slower                                                           |
| logging_silent           | 57.9 ns                                                             | 59.7 ns: 1.03x slower                                                           |
| async_tree_none_tg       | 203 ms                                                              | 210 ms: 1.03x slower                                                            |
| 2to3                     | 233 ms                                                              | 242 ms: 1.04x slower                                                            |
| genshi_text              | 20.1 ms                                                             | 20.9 ms: 1.04x slower                                                           |
| fannkuch                 | 270 ms                                                              | 282 ms: 1.04x slower                                                            |
| xml_etree_iterparse      | 64.2 ms                                                             | 67.1 ms: 1.04x slower                                                           |
| meteor_contest           | 74.1 ms                                                             | 77.5 ms: 1.05x slower                                                           |
| crypto_pyaes             | 55.8 ms                                                             | 58.4 ms: 1.05x slower                                                           |
| docutils                 | 1.81 sec                                                            | 1.90 sec: 1.05x slower                                                          |
| sympy_expand             | 375 ms                                                              | 394 ms: 1.05x slower                                                            |
| float                    | 52.4 ms                                                             | 55.1 ms: 1.05x slower                                                           |
| genshi_xml               | 44.3 ms                                                             | 46.8 ms: 1.06x slower                                                           |
| logging_format           | 8.13 us                                                             | 8.60 us: 1.06x slower                                                           |
| scimark_fft              | 198 ms                                                              | 209 ms: 1.06x slower                                                            |
| pylint                   | 217 ms                                                              | 230 ms: 1.06x slower                                                            |
| django_template          | 30.1 ms                                                             | 31.9 ms: 1.06x slower                                                           |
| logging_simple           | 7.47 us                                                             | 7.92 us: 1.06x slower                                                           |
| sympy_str                | 211 ms                                                              | 224 ms: 1.06x slower                                                            |
| deepcopy_memo            | 23.5 us                                                             | 25.0 us: 1.07x slower                                                           |
| sympy_sum                | 105 ms                                                              | 113 ms: 1.07x slower                                                            |
| sympy_integrate          | 14.6 ms                                                             | 15.8 ms: 1.08x slower                                                           |
| mdp                      | 1.60 sec                                                            | 1.72 sec: 1.08x slower                                                          |
| pyflate                  | 308 ms                                                              | 332 ms: 1.08x slower                                                            |
| scimark_sparse_mat_mult  | 2.87 ms                                                             | 3.10 ms: 1.08x slower                                                           |
| raytrace                 | 189 ms                                                              | 203 ms: 1.08x slower                                                            |
| sqlglot_optimize         | 39.7 ms                                                             | 42.9 ms: 1.08x slower                                                           |
| pycparser                | 777 ms                                                              | 842 ms: 1.08x slower                                                            |
| sqlglot_normalize        | 206 ms                                                              | 224 ms: 1.09x slower                                                            |
| chaos                    | 48.0 ms                                                             | 52.6 ms: 1.10x slower                                                           |
| async_generators         | 266 ms                                                              | 291 ms: 1.10x slower                                                            |
| generators               | 21.2 ms                                                             | 23.4 ms: 1.10x slower                                                           |
| unpickle_pure_python     | 147 us                                                              | 164 us: 1.12x slower                                                            |
| scimark_monte_carlo      | 45.2 ms                                                             | 50.8 ms: 1.13x slower                                                           |
| nqueens                  | 68.7 ms                                                             | 77.3 ms: 1.13x slower                                                           |
| thrift                   | 9.73 ms                                                             | 11.0 ms: 1.13x slower                                                           |
| deltablue                | 2.23 ms                                                             | 2.58 ms: 1.15x slower                                                           |
| comprehensions           | 11.9 us                                                             | 13.7 us: 1.15x slower                                                           |
| go                       | 101 ms                                                              | 116 ms: 1.16x slower                                                            |
| spectral_norm            | 68.0 ms                                                             | 79.5 ms: 1.17x slower                                                           |
| scimark_sor              | 81.0 ms                                                             | 95.3 ms: 1.18x slower                                                           |
| regex_compile            | 99.9 ms                                                             | 119 ms: 1.19x slower                                                            |
| hexiom                   | 4.23 ms                                                             | 5.39 ms: 1.27x slower                                                           |
| scimark_lu               | 59.4 ms                                                             | 80.9 ms: 1.36x slower                                                           |
| coverage                 | 307 ms                                                              | 512 ms: 1.67x slower                                                            |
| Geometric mean           | (ref)                                                               | 1.04x slower                                                                    |

Benchmark hidden because not significant (9): python_startup_no_site, gc_traversal, async_tree_cpu_io_mixed_tg, bench_mp_pool, async_tree_cpu_io_mixed, async_tree_io_tg, async_tree_io, async_tree_memoization, async_tree_memoization_tg
Ignored benchmarks (1) of results/bm-20240605-3.13.0b2-3a83b17/bm-20240605-pythonperf1_win32-x86-python-v3.13.0b2-3.13.0b2-3a83b17.json: flaskblogging

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.02x
- 95% likely to have a slowdown of 1.02x
- 99% likely to have a slowdown of 1.01x

# Memory
- memory change: unknown