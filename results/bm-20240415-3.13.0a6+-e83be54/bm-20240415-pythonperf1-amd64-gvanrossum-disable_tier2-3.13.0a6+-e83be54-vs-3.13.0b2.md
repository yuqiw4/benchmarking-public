# Results vs. 3.13.0b2

- fork: gvanrossum
- ref: disable_tier2
- machine: windows-amd64
- commit hash: e83be54
- commit date: 2024-04-15
- overall geometric mean: 1.03x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.02x slower
- Memory change: unknown

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240605-pythonperf1-amd64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240415-pythonperf1-amd64-gvanrossum-disable_tier2-3.13.0a6+-e83be54 |
|----------------|:---------------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 207 ms                                                          | 211 ms: 1.02x slower                                                     |
| docutils       | 1.63 sec                                                        | 1.65 sec: 1.02x slower                                                   |
| html5lib       | 35.0 ms                                                         | 37.4 ms: 1.07x slower                                                    |
| Geometric mean | (ref)                                                           | 1.02x slower                                                             |

Benchmark hidden because not significant (2): chameleon, tornado_http

Benchmarks with tag 'asyncio':
==============================

| Benchmark                 | bm-20240605-pythonperf1-amd64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240415-pythonperf1-amd64-gvanrossum-disable_tier2-3.13.0a6+-e83be54 |
|---------------------------|:---------------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_cpu_io_mixed   | 389 ms                                                          | 397 ms: 1.02x slower                                                     |
| async_tree_memoization    | 264 ms                                                          | 273 ms: 1.03x slower                                                     |
| async_tree_io_tg          | 605 ms                                                          | 626 ms: 1.03x slower                                                     |
| async_tree_none           | 218 ms                                                          | 227 ms: 1.04x slower                                                     |
| async_tree_memoization_tg | 258 ms                                                          | 273 ms: 1.06x slower                                                     |
| async_tree_none_tg        | 202 ms                                                          | 225 ms: 1.11x slower                                                     |
| Geometric mean            | (ref)                                                           | 1.04x slower                                                             |

Benchmark hidden because not significant (2): async_tree_cpu_io_mixed_tg, async_tree_io

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240605-pythonperf1-amd64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240415-pythonperf1-amd64-gvanrossum-disable_tier2-3.13.0a6+-e83be54 |
|----------------|:---------------------------------------------------------------:|:------------------------------------------------------------------------:|
| pidigits       | 150 ms                                                          | 147 ms: 1.02x faster                                                     |
| nbody          | 67.6 ms                                                         | 68.5 ms: 1.01x slower                                                    |
| float          | 49.7 ms                                                         | 50.9 ms: 1.02x slower                                                    |
| Geometric mean | (ref)                                                           | 1.01x slower                                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240605-pythonperf1-amd64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240415-pythonperf1-amd64-gvanrossum-disable_tier2-3.13.0a6+-e83be54 |
|----------------|:---------------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_dna      | 119 ms                                                          | 117 ms: 1.02x faster                                                     |
| regex_effbot   | 1.58 ms                                                         | 1.56 ms: 1.02x faster                                                    |
| regex_compile  | 78.0 ms                                                         | 78.9 ms: 1.01x slower                                                    |
| Geometric mean | (ref)                                                           | 1.01x faster                                                             |

Benchmark hidden because not significant (1): regex_v8

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240605-pythonperf1-amd64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240415-pythonperf1-amd64-gvanrossum-disable_tier2-3.13.0a6+-e83be54 |
|----------------------|:---------------------------------------------------------------:|:------------------------------------------------------------------------:|
| json_loads           | 14.2 us                                                         | 13.5 us: 1.05x faster                                                    |
| json_dumps           | 5.61 ms                                                         | 5.65 ms: 1.01x slower                                                    |
| pickle_dict          | 18.1 us                                                         | 18.4 us: 1.01x slower                                                    |
| xml_etree_iterparse  | 62.3 ms                                                         | 63.6 ms: 1.02x slower                                                    |
| xml_etree_parse      | 90.9 ms                                                         | 92.8 ms: 1.02x slower                                                    |
| pickle_pure_python   | 175 us                                                          | 180 us: 1.02x slower                                                     |
| xml_etree_generate   | 53.2 ms                                                         | 54.8 ms: 1.03x slower                                                    |
| xml_etree_process    | 36.4 ms                                                         | 37.6 ms: 1.03x slower                                                    |
| pickle               | 7.11 us                                                         | 7.37 us: 1.04x slower                                                    |
| unpickle_pure_python | 122 us                                                          | 128 us: 1.05x slower                                                     |
| tomli_loads          | 1.35 sec                                                        | 1.43 sec: 1.06x slower                                                   |
| pickle_list          | 2.90 us                                                         | 3.08 us: 1.06x slower                                                    |
| unpickle_list        | 2.62 us                                                         | 2.83 us: 1.08x slower                                                    |
| Geometric mean       | (ref)                                                           | 1.03x slower                                                             |

Benchmark hidden because not significant (1): unpickle

Benchmarks with tag 'startup':
==============================

| Benchmark      | bm-20240605-pythonperf1-amd64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240415-pythonperf1-amd64-gvanrossum-disable_tier2-3.13.0a6+-e83be54 |
|----------------|:---------------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup | 20.3 ms                                                         | 19.8 ms: 1.02x faster                                                    |
| Geometric mean | (ref)                                                           | 1.01x faster                                                             |

Benchmark hidden because not significant (1): python_startup_no_site

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240605-pythonperf1-amd64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240415-pythonperf1-amd64-gvanrossum-disable_tier2-3.13.0a6+-e83be54 |
|-----------------|:---------------------------------------------------------------:|:------------------------------------------------------------------------:|
| django_template | 21.7 ms                                                         | 23.6 ms: 1.09x slower                                                    |
| genshi_xml      | 31.6 ms                                                         | 34.4 ms: 1.09x slower                                                    |
| genshi_text     | 14.4 ms                                                         | 16.8 ms: 1.17x slower                                                    |
| Geometric mean  | (ref)                                                           | 1.08x slower                                                             |

Benchmark hidden because not significant (1): mako

All benchmarks:
===============

| Benchmark                 | bm-20240605-pythonperf1-amd64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240415-pythonperf1-amd64-gvanrossum-disable_tier2-3.13.0a6+-e83be54 |
|---------------------------|:---------------------------------------------------------------:|:------------------------------------------------------------------------:|
| typing_runtime_protocols  | 101 us                                                          | 75.5 us: 1.34x faster                                                    |
| scimark_lu                | 56.6 ms                                                         | 53.8 ms: 1.05x faster                                                    |
| json_loads                | 14.2 us                                                         | 13.5 us: 1.05x faster                                                    |
| spectral_norm             | 63.7 ms                                                         | 60.9 ms: 1.05x faster                                                    |
| scimark_sor               | 75.3 ms                                                         | 72.0 ms: 1.05x faster                                                    |
| thrift                    | 8.11 ms                                                         | 7.84 ms: 1.03x faster                                                    |
| python_startup            | 20.3 ms                                                         | 19.8 ms: 1.02x faster                                                    |
| crypto_pyaes              | 45.5 ms                                                         | 44.5 ms: 1.02x faster                                                    |
| regex_dna                 | 119 ms                                                          | 117 ms: 1.02x faster                                                     |
| pidigits                  | 150 ms                                                          | 147 ms: 1.02x faster                                                     |
| bench_mp_pool             | 64.8 ms                                                         | 63.7 ms: 1.02x faster                                                    |
| deepcopy_memo             | 22.1 us                                                         | 21.7 us: 1.02x faster                                                    |
| regex_effbot              | 1.58 ms                                                         | 1.56 ms: 1.02x faster                                                    |
| chaos                     | 38.4 ms                                                         | 38.1 ms: 1.01x faster                                                    |
| gc_traversal              | 1.55 ms                                                         | 1.55 ms: 1.01x faster                                                    |
| json_dumps                | 5.61 ms                                                         | 5.65 ms: 1.01x slower                                                    |
| regex_compile             | 78.0 ms                                                         | 78.9 ms: 1.01x slower                                                    |
| raytrace                  | 162 ms                                                          | 164 ms: 1.01x slower                                                     |
| deepcopy_reduce           | 1.99 us                                                         | 2.02 us: 1.01x slower                                                    |
| nbody                     | 67.6 ms                                                         | 68.5 ms: 1.01x slower                                                    |
| fannkuch                  | 243 ms                                                          | 247 ms: 1.01x slower                                                     |
| pickle_dict               | 18.1 us                                                         | 18.4 us: 1.01x slower                                                    |
| sympy_str                 | 159 ms                                                          | 161 ms: 1.01x slower                                                     |
| sympy_expand              | 271 ms                                                          | 275 ms: 1.02x slower                                                     |
| mypy2                     | 418 ms                                                          | 424 ms: 1.02x slower                                                     |
| docutils                  | 1.63 sec                                                        | 1.65 sec: 1.02x slower                                                   |
| hexiom                    | 3.72 ms                                                         | 3.79 ms: 1.02x slower                                                    |
| scimark_sparse_mat_mult   | 2.50 ms                                                         | 2.55 ms: 1.02x slower                                                    |
| comprehensions            | 10.4 us                                                         | 10.6 us: 1.02x slower                                                    |
| xml_etree_iterparse       | 62.3 ms                                                         | 63.6 ms: 1.02x slower                                                    |
| scimark_monte_carlo       | 39.1 ms                                                         | 39.9 ms: 1.02x slower                                                    |
| sympy_integrate           | 12.2 ms                                                         | 12.5 ms: 1.02x slower                                                    |
| async_tree_cpu_io_mixed   | 389 ms                                                          | 397 ms: 1.02x slower                                                     |
| xml_etree_parse           | 90.9 ms                                                         | 92.8 ms: 1.02x slower                                                    |
| sqlglot_parse             | 748 us                                                          | 764 us: 1.02x slower                                                     |
| 2to3                      | 207 ms                                                          | 211 ms: 1.02x slower                                                     |
| pickle_pure_python        | 175 us                                                          | 180 us: 1.02x slower                                                     |
| float                     | 49.7 ms                                                         | 50.9 ms: 1.02x slower                                                    |
| sqlglot_transpile         | 955 us                                                          | 979 us: 1.03x slower                                                     |
| deepcopy                  | 220 us                                                          | 226 us: 1.03x slower                                                     |
| pyflate                   | 279 ms                                                          | 286 ms: 1.03x slower                                                     |
| pprint_safe_repr          | 474 ms                                                          | 489 ms: 1.03x slower                                                     |
| xml_etree_generate        | 53.2 ms                                                         | 54.8 ms: 1.03x slower                                                    |
| pprint_pformat            | 966 ms                                                          | 996 ms: 1.03x slower                                                     |
| xml_etree_process         | 36.4 ms                                                         | 37.6 ms: 1.03x slower                                                    |
| logging_simple            | 5.78 us                                                         | 5.98 us: 1.03x slower                                                    |
| async_tree_memoization    | 264 ms                                                          | 273 ms: 1.03x slower                                                     |
| async_tree_io_tg          | 605 ms                                                          | 626 ms: 1.03x slower                                                     |
| pickle                    | 7.11 us                                                         | 7.37 us: 1.04x slower                                                    |
| logging_format            | 6.22 us                                                         | 6.46 us: 1.04x slower                                                    |
| sqlite_synth              | 1.60 us                                                         | 1.66 us: 1.04x slower                                                    |
| nqueens                   | 56.7 ms                                                         | 58.9 ms: 1.04x slower                                                    |
| async_tree_none           | 218 ms                                                          | 227 ms: 1.04x slower                                                     |
| coroutines                | 12.8 ms                                                         | 13.3 ms: 1.04x slower                                                    |
| dulwich_log               | 38.0 ms                                                         | 39.9 ms: 1.05x slower                                                    |
| bench_thread_pool         | 768 us                                                          | 807 us: 1.05x slower                                                     |
| async_generators          | 223 ms                                                          | 235 ms: 1.05x slower                                                     |
| unpickle_pure_python      | 122 us                                                          | 128 us: 1.05x slower                                                     |
| async_tree_memoization_tg | 258 ms                                                          | 273 ms: 1.06x slower                                                     |
| tomli_loads               | 1.35 sec                                                        | 1.43 sec: 1.06x slower                                                   |
| mdp                       | 1.31 sec                                                        | 1.39 sec: 1.06x slower                                                   |
| pickle_list               | 2.90 us                                                         | 3.08 us: 1.06x slower                                                    |
| sqlglot_optimize          | 32.7 ms                                                         | 34.7 ms: 1.06x slower                                                    |
| meteor_contest            | 69.9 ms                                                         | 74.2 ms: 1.06x slower                                                    |
| scimark_fft               | 171 ms                                                          | 182 ms: 1.06x slower                                                     |
| sqlglot_normalize         | 173 ms                                                          | 185 ms: 1.07x slower                                                     |
| html5lib                  | 35.0 ms                                                         | 37.4 ms: 1.07x slower                                                    |
| generators                | 19.6 ms                                                         | 20.9 ms: 1.07x slower                                                    |
| logging_silent            | 52.9 ns                                                         | 56.8 ns: 1.07x slower                                                    |
| unpickle_list             | 2.62 us                                                         | 2.83 us: 1.08x slower                                                    |
| django_template           | 21.7 ms                                                         | 23.6 ms: 1.09x slower                                                    |
| genshi_xml                | 31.6 ms                                                         | 34.4 ms: 1.09x slower                                                    |
| telco                     | 4.67 ms                                                         | 5.10 ms: 1.09x slower                                                    |
| coverage                  | 42.1 ms                                                         | 46.0 ms: 1.09x slower                                                    |
| deltablue                 | 1.88 ms                                                         | 2.06 ms: 1.10x slower                                                    |
| richards                  | 26.7 ms                                                         | 29.3 ms: 1.10x slower                                                    |
| richards_super            | 30.2 ms                                                         | 33.3 ms: 1.10x slower                                                    |
| go                        | 82.1 ms                                                         | 90.8 ms: 1.11x slower                                                    |
| async_tree_none_tg        | 202 ms                                                          | 225 ms: 1.11x slower                                                     |
| genshi_text               | 14.4 ms                                                         | 16.8 ms: 1.17x slower                                                    |
| asyncio_tcp_ssl           | 1.48 sec                                                        | 1.79 sec: 1.21x slower                                                   |
| Geometric mean            | (ref)                                                           | 1.03x slower                                                             |

Benchmark hidden because not significant (16): regex_v8, aiohttp, mako, pycparser, unpickle, sympy_sum, tornado_http, pathlib, python_startup_no_site, chameleon, create_gc_cycles, json, asyncio_tcp, async_tree_cpu_io_mixed_tg, pylint, async_tree_io
Ignored benchmarks (1) of results/bm-20240605-3.13.0b2-3a83b17/bm-20240605-pythonperf1-amd64-python-v3.13.0b2-3.13.0b2-3a83b17.json: flaskblogging

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.02x
- 95% likely to have a slowdown of 1.02x
- 99% likely to have a slowdown of 1.02x

# Memory
- memory change: unknown