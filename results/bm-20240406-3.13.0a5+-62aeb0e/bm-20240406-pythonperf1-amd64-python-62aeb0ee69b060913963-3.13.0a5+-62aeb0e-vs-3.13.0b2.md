# Results vs. 3.13.0b2

- fork: python
- ref: 62aeb0ee69b060913963
- machine: windows-amd64
- commit hash: 62aeb0e
- commit date: 2024-04-06
- overall geometric mean: 1.04x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.03x slower
- Memory change: unknown

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240605-pythonperf1-amd64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240406-pythonperf1-amd64-python-62aeb0ee69b060913963-3.13.0a5+-62aeb0e |
|----------------|:---------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| 2to3           | 207 ms                                                          | 214 ms: 1.04x slower                                                        |
| chameleon      | 4.80 ms                                                         | 5.01 ms: 1.04x slower                                                       |
| docutils       | 1.63 sec                                                        | 1.64 sec: 1.01x slower                                                      |
| html5lib       | 35.0 ms                                                         | 36.7 ms: 1.05x slower                                                       |
| tornado_http   | 81.8 ms                                                         | 83.9 ms: 1.03x slower                                                       |
| Geometric mean | (ref)                                                           | 1.03x slower                                                                |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                 | bm-20240605-pythonperf1-amd64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240406-pythonperf1-amd64-python-62aeb0ee69b060913963-3.13.0a5+-62aeb0e |
|---------------------------|:---------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| async_tree_io_tg          | 605 ms                                                          | 627 ms: 1.04x slower                                                        |
| async_tree_none           | 218 ms                                                          | 229 ms: 1.05x slower                                                        |
| async_tree_memoization_tg | 258 ms                                                          | 272 ms: 1.05x slower                                                        |
| async_tree_memoization    | 264 ms                                                          | 278 ms: 1.05x slower                                                        |
| async_tree_none_tg        | 202 ms                                                          | 221 ms: 1.09x slower                                                        |
| Geometric mean            | (ref)                                                           | 1.04x slower                                                                |

Benchmark hidden because not significant (3): async_tree_io, async_tree_cpu_io_mixed_tg, async_tree_cpu_io_mixed

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240605-pythonperf1-amd64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240406-pythonperf1-amd64-python-62aeb0ee69b060913963-3.13.0a5+-62aeb0e |
|----------------|:---------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| pidigits       | 150 ms                                                          | 147 ms: 1.02x faster                                                        |
| float          | 49.7 ms                                                         | 52.8 ms: 1.06x slower                                                       |
| nbody          | 67.6 ms                                                         | 74.1 ms: 1.10x slower                                                       |
| Geometric mean | (ref)                                                           | 1.04x slower                                                                |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240605-pythonperf1-amd64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240406-pythonperf1-amd64-python-62aeb0ee69b060913963-3.13.0a5+-62aeb0e |
|----------------|:---------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| regex_dna      | 119 ms                                                          | 120 ms: 1.01x slower                                                        |
| regex_compile  | 78.0 ms                                                         | 81.2 ms: 1.04x slower                                                       |
| Geometric mean | (ref)                                                           | 1.02x slower                                                                |

Benchmark hidden because not significant (2): regex_effbot, regex_v8

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240605-pythonperf1-amd64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240406-pythonperf1-amd64-python-62aeb0ee69b060913963-3.13.0a5+-62aeb0e |
|----------------------|:---------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| json_loads           | 14.2 us                                                         | 13.8 us: 1.03x faster                                                       |
| json_dumps           | 5.61 ms                                                         | 5.72 ms: 1.02x slower                                                       |
| unpickle             | 8.40 us                                                         | 8.63 us: 1.03x slower                                                       |
| xml_etree_iterparse  | 62.3 ms                                                         | 64.7 ms: 1.04x slower                                                       |
| pickle_dict          | 18.1 us                                                         | 18.9 us: 1.04x slower                                                       |
| xml_etree_process    | 36.4 ms                                                         | 38.1 ms: 1.05x slower                                                       |
| xml_etree_generate   | 53.2 ms                                                         | 55.7 ms: 1.05x slower                                                       |
| pickle_pure_python   | 175 us                                                          | 185 us: 1.05x slower                                                        |
| pickle               | 7.11 us                                                         | 7.52 us: 1.06x slower                                                       |
| unpickle_list        | 2.62 us                                                         | 2.80 us: 1.07x slower                                                       |
| tomli_loads          | 1.35 sec                                                        | 1.45 sec: 1.07x slower                                                      |
| unpickle_pure_python | 122 us                                                          | 138 us: 1.13x slower                                                        |
| Geometric mean       | (ref)                                                           | 1.04x slower                                                                |

Benchmark hidden because not significant (2): xml_etree_parse, pickle_list

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240605-pythonperf1-amd64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240406-pythonperf1-amd64-python-62aeb0ee69b060913963-3.13.0a5+-62aeb0e |
|------------------------|:---------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| python_startup         | 20.3 ms                                                         | 19.9 ms: 1.02x faster                                                       |
| python_startup_no_site | 16.2 ms                                                         | 17.8 ms: 1.10x slower                                                       |
| Geometric mean         | (ref)                                                           | 1.04x slower                                                                |

Benchmarks with tag 'template':
===============================

| Benchmark      | bm-20240605-pythonperf1-amd64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240406-pythonperf1-amd64-python-62aeb0ee69b060913963-3.13.0a5+-62aeb0e |
|----------------|:---------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| mako           | 6.36 ms                                                         | 6.51 ms: 1.02x slower                                                       |
| genshi_xml     | 31.6 ms                                                         | 36.4 ms: 1.15x slower                                                       |
| genshi_text    | 14.4 ms                                                         | 16.7 ms: 1.17x slower                                                       |
| Geometric mean | (ref)                                                           | 1.11x slower                                                                |

All benchmarks:
===============

| Benchmark                 | bm-20240605-pythonperf1-amd64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240406-pythonperf1-amd64-python-62aeb0ee69b060913963-3.13.0a5+-62aeb0e |
|---------------------------|:---------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| typing_runtime_protocols  | 101 us                                                          | 75.0 us: 1.35x faster                                                       |
| json                      | 3.19 ms                                                         | 2.88 ms: 1.11x faster                                                       |
| pylint                    | 205 ms                                                          | 187 ms: 1.10x faster                                                        |
| json_loads                | 14.2 us                                                         | 13.8 us: 1.03x faster                                                       |
| pidigits                  | 150 ms                                                          | 147 ms: 1.02x faster                                                        |
| python_startup            | 20.3 ms                                                         | 19.9 ms: 1.02x faster                                                       |
| gc_traversal              | 1.55 ms                                                         | 1.54 ms: 1.01x faster                                                       |
| regex_dna                 | 119 ms                                                          | 120 ms: 1.01x slower                                                        |
| docutils                  | 1.63 sec                                                        | 1.64 sec: 1.01x slower                                                      |
| thrift                    | 8.11 ms                                                         | 8.18 ms: 1.01x slower                                                       |
| sympy_sum                 | 84.4 ms                                                         | 85.2 ms: 1.01x slower                                                       |
| sqlite_synth              | 1.60 us                                                         | 1.62 us: 1.01x slower                                                       |
| json_dumps                | 5.61 ms                                                         | 5.72 ms: 1.02x slower                                                       |
| mypy2                     | 418 ms                                                          | 427 ms: 1.02x slower                                                        |
| spectral_norm             | 63.7 ms                                                         | 65.2 ms: 1.02x slower                                                       |
| mako                      | 6.36 ms                                                         | 6.51 ms: 1.02x slower                                                       |
| tornado_http              | 81.8 ms                                                         | 83.9 ms: 1.03x slower                                                       |
| sympy_expand              | 271 ms                                                          | 277 ms: 1.03x slower                                                        |
| deepcopy_reduce           | 1.99 us                                                         | 2.05 us: 1.03x slower                                                       |
| unpickle                  | 8.40 us                                                         | 8.63 us: 1.03x slower                                                       |
| asyncio_tcp               | 471 ms                                                          | 484 ms: 1.03x slower                                                        |
| pathlib                   | 75.9 ms                                                         | 78.0 ms: 1.03x slower                                                       |
| sympy_integrate           | 12.2 ms                                                         | 12.6 ms: 1.03x slower                                                       |
| sympy_str                 | 159 ms                                                          | 164 ms: 1.03x slower                                                        |
| 2to3                      | 207 ms                                                          | 214 ms: 1.04x slower                                                        |
| async_tree_io_tg          | 605 ms                                                          | 627 ms: 1.04x slower                                                        |
| crypto_pyaes              | 45.5 ms                                                         | 47.1 ms: 1.04x slower                                                       |
| xml_etree_iterparse       | 62.3 ms                                                         | 64.7 ms: 1.04x slower                                                       |
| deepcopy                  | 220 us                                                          | 228 us: 1.04x slower                                                        |
| logging_format            | 6.22 us                                                         | 6.47 us: 1.04x slower                                                       |
| regex_compile             | 78.0 ms                                                         | 81.2 ms: 1.04x slower                                                       |
| sqlglot_transpile         | 955 us                                                          | 994 us: 1.04x slower                                                        |
| chameleon                 | 4.80 ms                                                         | 5.01 ms: 1.04x slower                                                       |
| pickle_dict               | 18.1 us                                                         | 18.9 us: 1.04x slower                                                       |
| chaos                     | 38.4 ms                                                         | 40.1 ms: 1.04x slower                                                       |
| deepcopy_memo             | 22.1 us                                                         | 23.1 us: 1.05x slower                                                       |
| xml_etree_process         | 36.4 ms                                                         | 38.1 ms: 1.05x slower                                                       |
| async_generators          | 223 ms                                                          | 234 ms: 1.05x slower                                                        |
| pprint_pformat            | 966 ms                                                          | 1.01 sec: 1.05x slower                                                      |
| xml_etree_generate        | 53.2 ms                                                         | 55.7 ms: 1.05x slower                                                       |
| html5lib                  | 35.0 ms                                                         | 36.7 ms: 1.05x slower                                                       |
| sqlglot_parse             | 748 us                                                          | 785 us: 1.05x slower                                                        |
| pprint_safe_repr          | 474 ms                                                          | 498 ms: 1.05x slower                                                        |
| raytrace                  | 162 ms                                                          | 171 ms: 1.05x slower                                                        |
| sqlglot_normalize         | 173 ms                                                          | 182 ms: 1.05x slower                                                        |
| async_tree_none           | 218 ms                                                          | 229 ms: 1.05x slower                                                        |
| async_tree_memoization_tg | 258 ms                                                          | 272 ms: 1.05x slower                                                        |
| async_tree_memoization    | 264 ms                                                          | 278 ms: 1.05x slower                                                        |
| logging_simple            | 5.78 us                                                         | 6.09 us: 1.05x slower                                                       |
| pickle_pure_python        | 175 us                                                          | 185 us: 1.05x slower                                                        |
| sqlglot_optimize          | 32.7 ms                                                         | 34.5 ms: 1.05x slower                                                       |
| meteor_contest            | 69.9 ms                                                         | 73.9 ms: 1.06x slower                                                       |
| pickle                    | 7.11 us                                                         | 7.52 us: 1.06x slower                                                       |
| pyflate                   | 279 ms                                                          | 296 ms: 1.06x slower                                                        |
| coroutines                | 12.8 ms                                                         | 13.5 ms: 1.06x slower                                                       |
| float                     | 49.7 ms                                                         | 52.8 ms: 1.06x slower                                                       |
| scimark_lu                | 56.6 ms                                                         | 60.1 ms: 1.06x slower                                                       |
| scimark_sor               | 75.3 ms                                                         | 80.1 ms: 1.06x slower                                                       |
| mdp                       | 1.31 sec                                                        | 1.40 sec: 1.07x slower                                                      |
| telco                     | 4.67 ms                                                         | 4.98 ms: 1.07x slower                                                       |
| unpickle_list             | 2.62 us                                                         | 2.80 us: 1.07x slower                                                       |
| nqueens                   | 56.7 ms                                                         | 60.5 ms: 1.07x slower                                                       |
| bench_thread_pool         | 768 us                                                          | 823 us: 1.07x slower                                                        |
| tomli_loads               | 1.35 sec                                                        | 1.45 sec: 1.07x slower                                                      |
| dulwich_log               | 38.0 ms                                                         | 41.0 ms: 1.08x slower                                                       |
| generators                | 19.6 ms                                                         | 21.1 ms: 1.08x slower                                                       |
| scimark_sparse_mat_mult   | 2.50 ms                                                         | 2.71 ms: 1.08x slower                                                       |
| scimark_fft               | 171 ms                                                          | 186 ms: 1.09x slower                                                        |
| fannkuch                  | 243 ms                                                          | 265 ms: 1.09x slower                                                        |
| coverage                  | 42.1 ms                                                         | 45.8 ms: 1.09x slower                                                       |
| async_tree_none_tg        | 202 ms                                                          | 221 ms: 1.09x slower                                                        |
| nbody                     | 67.6 ms                                                         | 74.1 ms: 1.10x slower                                                       |
| scimark_monte_carlo       | 39.1 ms                                                         | 42.9 ms: 1.10x slower                                                       |
| logging_silent            | 52.9 ns                                                         | 58.0 ns: 1.10x slower                                                       |
| python_startup_no_site    | 16.2 ms                                                         | 17.8 ms: 1.10x slower                                                       |
| comprehensions            | 10.4 us                                                         | 11.4 us: 1.10x slower                                                       |
| hexiom                    | 3.72 ms                                                         | 4.09 ms: 1.10x slower                                                       |
| deltablue                 | 1.88 ms                                                         | 2.11 ms: 1.12x slower                                                       |
| go                        | 82.1 ms                                                         | 92.1 ms: 1.12x slower                                                       |
| richards_super            | 30.2 ms                                                         | 34.1 ms: 1.13x slower                                                       |
| unpickle_pure_python      | 122 us                                                          | 138 us: 1.13x slower                                                        |
| richards                  | 26.7 ms                                                         | 30.5 ms: 1.14x slower                                                       |
| genshi_xml                | 31.6 ms                                                         | 36.4 ms: 1.15x slower                                                       |
| genshi_text               | 14.4 ms                                                         | 16.7 ms: 1.17x slower                                                       |
| asyncio_tcp_ssl           | 1.48 sec                                                        | 1.78 sec: 1.20x slower                                                      |
| Geometric mean            | (ref)                                                           | 1.04x slower                                                                |

Benchmark hidden because not significant (11): pycparser, bench_mp_pool, regex_effbot, async_tree_io, create_gc_cycles, async_tree_cpu_io_mixed_tg, aiohttp, xml_etree_parse, pickle_list, async_tree_cpu_io_mixed, regex_v8
Ignored benchmarks (2) of results/bm-20240605-3.13.0b2-3a83b17/bm-20240605-pythonperf1-amd64-python-v3.13.0b2-3.13.0b2-3a83b17.json: django_template, flaskblogging

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.03x
- 95% likely to have a slowdown of 1.03x
- 99% likely to have a slowdown of 1.03x

# Memory
- memory change: unknown