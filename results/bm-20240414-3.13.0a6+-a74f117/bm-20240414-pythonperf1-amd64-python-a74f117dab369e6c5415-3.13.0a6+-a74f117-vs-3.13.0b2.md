# Results vs. 3.13.0b2

- fork: python
- ref: a74f117dab369e6c5415
- machine: windows-amd64
- commit hash: a74f117
- commit date: 2024-04-14
- overall geometric mean: 1.03x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.02x slower
- Memory change: unknown

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240605-pythonperf1-amd64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240414-pythonperf1-amd64-python-a74f117dab369e6c5415-3.13.0a6+-a74f117 |
|----------------|:---------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| 2to3           | 207 ms                                                          | 210 ms: 1.02x slower                                                        |
| chameleon      | 4.80 ms                                                         | 5.01 ms: 1.04x slower                                                       |
| docutils       | 1.63 sec                                                        | 1.64 sec: 1.01x slower                                                      |
| html5lib       | 35.0 ms                                                         | 36.2 ms: 1.03x slower                                                       |
| Geometric mean | (ref)                                                           | 1.02x slower                                                                |

Benchmark hidden because not significant (1): tornado_http

Benchmarks with tag 'asyncio':
==============================

| Benchmark              | bm-20240605-pythonperf1-amd64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240414-pythonperf1-amd64-python-a74f117dab369e6c5415-3.13.0a6+-a74f117 |
|------------------------|:---------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| async_tree_io_tg       | 605 ms                                                          | 620 ms: 1.02x slower                                                        |
| async_tree_none        | 218 ms                                                          | 224 ms: 1.03x slower                                                        |
| async_tree_memoization | 264 ms                                                          | 272 ms: 1.03x slower                                                        |
| async_tree_none_tg     | 202 ms                                                          | 222 ms: 1.10x slower                                                        |
| Geometric mean         | (ref)                                                           | 1.03x slower                                                                |

Benchmark hidden because not significant (4): async_tree_cpu_io_mixed_tg, async_tree_cpu_io_mixed, async_tree_io, async_tree_memoization_tg

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240605-pythonperf1-amd64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240414-pythonperf1-amd64-python-a74f117dab369e6c5415-3.13.0a6+-a74f117 |
|----------------|:---------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| pidigits       | 150 ms                                                          | 147 ms: 1.02x faster                                                        |
| nbody          | 67.6 ms                                                         | 70.2 ms: 1.04x slower                                                       |
| float          | 49.7 ms                                                         | 51.6 ms: 1.04x slower                                                       |
| Geometric mean | (ref)                                                           | 1.02x slower                                                                |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240605-pythonperf1-amd64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240414-pythonperf1-amd64-python-a74f117dab369e6c5415-3.13.0a6+-a74f117 |
|----------------|:---------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| regex_effbot   | 1.58 ms                                                         | 1.59 ms: 1.00x slower                                                       |
| regex_dna      | 119 ms                                                          | 122 ms: 1.02x slower                                                        |
| regex_compile  | 78.0 ms                                                         | 79.8 ms: 1.02x slower                                                       |
| Geometric mean | (ref)                                                           | 1.02x slower                                                                |

Benchmark hidden because not significant (1): regex_v8

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240605-pythonperf1-amd64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240414-pythonperf1-amd64-python-a74f117dab369e6c5415-3.13.0a6+-a74f117 |
|----------------------|:---------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| json_loads           | 14.2 us                                                         | 13.8 us: 1.03x faster                                                       |
| pickle               | 7.11 us                                                         | 7.14 us: 1.00x slower                                                       |
| json_dumps           | 5.61 ms                                                         | 5.64 ms: 1.00x slower                                                       |
| pickle_pure_python   | 175 us                                                          | 179 us: 1.02x slower                                                        |
| pickle_dict          | 18.1 us                                                         | 18.6 us: 1.02x slower                                                       |
| xml_etree_iterparse  | 62.3 ms                                                         | 64.0 ms: 1.03x slower                                                       |
| xml_etree_process    | 36.4 ms                                                         | 37.7 ms: 1.03x slower                                                       |
| xml_etree_generate   | 53.2 ms                                                         | 55.3 ms: 1.04x slower                                                       |
| tomli_loads          | 1.35 sec                                                        | 1.41 sec: 1.04x slower                                                      |
| unpickle_pure_python | 122 us                                                          | 129 us: 1.06x slower                                                        |
| unpickle_list        | 2.62 us                                                         | 2.80 us: 1.07x slower                                                       |
| Geometric mean       | (ref)                                                           | 1.02x slower                                                                |

Benchmark hidden because not significant (3): unpickle, xml_etree_parse, pickle_list

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240605-pythonperf1-amd64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240414-pythonperf1-amd64-python-a74f117dab369e6c5415-3.13.0a6+-a74f117 |
|------------------------|:---------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| python_startup_no_site | 16.2 ms                                                         | 17.0 ms: 1.05x slower                                                       |
| Geometric mean         | (ref)                                                           | 1.02x slower                                                                |

Benchmark hidden because not significant (1): python_startup

Benchmarks with tag 'template':
===============================

| Benchmark      | bm-20240605-pythonperf1-amd64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240414-pythonperf1-amd64-python-a74f117dab369e6c5415-3.13.0a6+-a74f117 |
|----------------|:---------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| genshi_xml     | 31.6 ms                                                         | 35.6 ms: 1.13x slower                                                       |
| genshi_text    | 14.4 ms                                                         | 16.5 ms: 1.15x slower                                                       |
| Geometric mean | (ref)                                                           | 1.09x slower                                                                |

Benchmark hidden because not significant (1): mako

All benchmarks:
===============

| Benchmark                | bm-20240605-pythonperf1-amd64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240414-pythonperf1-amd64-python-a74f117dab369e6c5415-3.13.0a6+-a74f117 |
|--------------------------|:---------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| typing_runtime_protocols | 101 us                                                          | 73.8 us: 1.37x faster                                                       |
| pylint                   | 205 ms                                                          | 188 ms: 1.09x faster                                                        |
| json_loads               | 14.2 us                                                         | 13.8 us: 1.03x faster                                                       |
| pidigits                 | 150 ms                                                          | 147 ms: 1.02x faster                                                        |
| thrift                   | 8.11 ms                                                         | 8.03 ms: 1.01x faster                                                       |
| bench_mp_pool            | 64.8 ms                                                         | 64.2 ms: 1.01x faster                                                       |
| pathlib                  | 75.9 ms                                                         | 75.2 ms: 1.01x faster                                                       |
| spectral_norm            | 63.7 ms                                                         | 63.3 ms: 1.01x faster                                                       |
| gc_traversal             | 1.55 ms                                                         | 1.55 ms: 1.01x faster                                                       |
| pickle                   | 7.11 us                                                         | 7.14 us: 1.00x slower                                                       |
| json_dumps               | 5.61 ms                                                         | 5.64 ms: 1.00x slower                                                       |
| regex_effbot             | 1.58 ms                                                         | 1.59 ms: 1.00x slower                                                       |
| crypto_pyaes             | 45.5 ms                                                         | 45.7 ms: 1.01x slower                                                       |
| scimark_lu               | 56.6 ms                                                         | 57.0 ms: 1.01x slower                                                       |
| deepcopy                 | 220 us                                                          | 222 us: 1.01x slower                                                        |
| docutils                 | 1.63 sec                                                        | 1.64 sec: 1.01x slower                                                      |
| deepcopy_memo            | 22.1 us                                                         | 22.3 us: 1.01x slower                                                       |
| deepcopy_reduce          | 1.99 us                                                         | 2.02 us: 1.01x slower                                                       |
| sympy_sum                | 84.4 ms                                                         | 85.4 ms: 1.01x slower                                                       |
| sympy_expand             | 271 ms                                                          | 274 ms: 1.01x slower                                                        |
| 2to3                     | 207 ms                                                          | 210 ms: 1.02x slower                                                        |
| scimark_sor              | 75.3 ms                                                         | 76.6 ms: 1.02x slower                                                       |
| raytrace                 | 162 ms                                                          | 165 ms: 1.02x slower                                                        |
| sympy_str                | 159 ms                                                          | 163 ms: 1.02x slower                                                        |
| chaos                    | 38.4 ms                                                         | 39.2 ms: 1.02x slower                                                       |
| pickle_pure_python       | 175 us                                                          | 179 us: 1.02x slower                                                        |
| pickle_dict              | 18.1 us                                                         | 18.6 us: 1.02x slower                                                       |
| regex_dna                | 119 ms                                                          | 122 ms: 1.02x slower                                                        |
| regex_compile            | 78.0 ms                                                         | 79.8 ms: 1.02x slower                                                       |
| async_tree_io_tg         | 605 ms                                                          | 620 ms: 1.02x slower                                                        |
| xml_etree_iterparse      | 62.3 ms                                                         | 64.0 ms: 1.03x slower                                                       |
| sqlite_synth             | 1.60 us                                                         | 1.64 us: 1.03x slower                                                       |
| sqlglot_transpile        | 955 us                                                          | 982 us: 1.03x slower                                                        |
| async_tree_none          | 218 ms                                                          | 224 ms: 1.03x slower                                                        |
| logging_format           | 6.22 us                                                         | 6.42 us: 1.03x slower                                                       |
| async_tree_memoization   | 264 ms                                                          | 272 ms: 1.03x slower                                                        |
| sympy_integrate          | 12.2 ms                                                         | 12.6 ms: 1.03x slower                                                       |
| xml_etree_process        | 36.4 ms                                                         | 37.7 ms: 1.03x slower                                                       |
| logging_simple           | 5.78 us                                                         | 5.98 us: 1.03x slower                                                       |
| html5lib                 | 35.0 ms                                                         | 36.2 ms: 1.03x slower                                                       |
| coroutines               | 12.8 ms                                                         | 13.2 ms: 1.04x slower                                                       |
| pyflate                  | 279 ms                                                          | 289 ms: 1.04x slower                                                        |
| pprint_safe_repr         | 474 ms                                                          | 491 ms: 1.04x slower                                                        |
| sqlglot_normalize        | 173 ms                                                          | 179 ms: 1.04x slower                                                        |
| sqlglot_parse            | 748 us                                                          | 776 us: 1.04x slower                                                        |
| scimark_monte_carlo      | 39.1 ms                                                         | 40.6 ms: 1.04x slower                                                       |
| pprint_pformat           | 966 ms                                                          | 1.00 sec: 1.04x slower                                                      |
| comprehensions           | 10.4 us                                                         | 10.8 us: 1.04x slower                                                       |
| sqlglot_optimize         | 32.7 ms                                                         | 34.0 ms: 1.04x slower                                                       |
| nbody                    | 67.6 ms                                                         | 70.2 ms: 1.04x slower                                                       |
| float                    | 49.7 ms                                                         | 51.6 ms: 1.04x slower                                                       |
| hexiom                   | 3.72 ms                                                         | 3.87 ms: 1.04x slower                                                       |
| xml_etree_generate       | 53.2 ms                                                         | 55.3 ms: 1.04x slower                                                       |
| meteor_contest           | 69.9 ms                                                         | 72.8 ms: 1.04x slower                                                       |
| chameleon                | 4.80 ms                                                         | 5.01 ms: 1.04x slower                                                       |
| tomli_loads              | 1.35 sec                                                        | 1.41 sec: 1.04x slower                                                      |
| python_startup_no_site   | 16.2 ms                                                         | 17.0 ms: 1.05x slower                                                       |
| async_generators         | 223 ms                                                          | 235 ms: 1.05x slower                                                        |
| bench_thread_pool        | 768 us                                                          | 811 us: 1.06x slower                                                        |
| unpickle_pure_python     | 122 us                                                          | 129 us: 1.06x slower                                                        |
| fannkuch                 | 243 ms                                                          | 257 ms: 1.06x slower                                                        |
| dulwich_log              | 38.0 ms                                                         | 40.3 ms: 1.06x slower                                                       |
| richards                 | 26.7 ms                                                         | 28.3 ms: 1.06x slower                                                       |
| scimark_sparse_mat_mult  | 2.50 ms                                                         | 2.66 ms: 1.06x slower                                                       |
| unpickle_list            | 2.62 us                                                         | 2.80 us: 1.07x slower                                                       |
| richards_super           | 30.2 ms                                                         | 32.3 ms: 1.07x slower                                                       |
| logging_silent           | 52.9 ns                                                         | 56.8 ns: 1.07x slower                                                       |
| nqueens                  | 56.7 ms                                                         | 60.8 ms: 1.07x slower                                                       |
| scimark_fft              | 171 ms                                                          | 185 ms: 1.08x slower                                                        |
| deltablue                | 1.88 ms                                                         | 2.04 ms: 1.08x slower                                                       |
| telco                    | 4.67 ms                                                         | 5.05 ms: 1.08x slower                                                       |
| coverage                 | 42.1 ms                                                         | 46.0 ms: 1.09x slower                                                       |
| go                       | 82.1 ms                                                         | 90.0 ms: 1.10x slower                                                       |
| async_tree_none_tg       | 202 ms                                                          | 222 ms: 1.10x slower                                                        |
| generators               | 19.6 ms                                                         | 21.7 ms: 1.11x slower                                                       |
| genshi_xml               | 31.6 ms                                                         | 35.6 ms: 1.13x slower                                                       |
| mdp                      | 1.31 sec                                                        | 1.49 sec: 1.13x slower                                                      |
| asyncio_tcp_ssl          | 1.48 sec                                                        | 1.68 sec: 1.14x slower                                                      |
| genshi_text              | 14.4 ms                                                         | 16.5 ms: 1.15x slower                                                       |
| Geometric mean           | (ref)                                                           | 1.03x slower                                                                |

Benchmark hidden because not significant (17): json, unpickle, aiohttp, python_startup, mypy2, xml_etree_parse, mako, tornado_http, create_gc_cycles, async_tree_cpu_io_mixed_tg, pickle_list, async_tree_cpu_io_mixed, regex_v8, async_tree_io, asyncio_tcp, pycparser, async_tree_memoization_tg
Ignored benchmarks (2) of results/bm-20240605-3.13.0b2-3a83b17/bm-20240605-pythonperf1-amd64-python-v3.13.0b2-3.13.0b2-3a83b17.json: django_template, flaskblogging

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.02x
- 95% likely to have a slowdown of 1.02x
- 99% likely to have a slowdown of 1.02x

# Memory
- memory change: unknown