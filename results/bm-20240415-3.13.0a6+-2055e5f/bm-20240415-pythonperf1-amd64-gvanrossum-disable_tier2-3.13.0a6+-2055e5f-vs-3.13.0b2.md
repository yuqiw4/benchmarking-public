# Results vs. 3.13.0b2

- fork: gvanrossum
- ref: disable_tier2
- machine: windows-amd64
- commit hash: 2055e5f
- commit date: 2024-04-15
- overall geometric mean: 1.03x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.02x slower
- Memory change: unknown

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240605-pythonperf1-amd64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240415-pythonperf1-amd64-gvanrossum-disable_tier2-3.13.0a6+-2055e5f |
|----------------|:---------------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 207 ms                                                          | 211 ms: 1.02x slower                                                     |
| chameleon      | 4.80 ms                                                         | 4.87 ms: 1.01x slower                                                    |
| docutils       | 1.63 sec                                                        | 1.65 sec: 1.02x slower                                                   |
| html5lib       | 35.0 ms                                                         | 36.8 ms: 1.05x slower                                                    |
| tornado_http   | 81.8 ms                                                         | 82.6 ms: 1.01x slower                                                    |
| Geometric mean | (ref)                                                           | 1.02x slower                                                             |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                 | bm-20240605-pythonperf1-amd64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240415-pythonperf1-amd64-gvanrossum-disable_tier2-3.13.0a6+-2055e5f |
|---------------------------|:---------------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_cpu_io_mixed   | 389 ms                                                          | 399 ms: 1.02x slower                                                     |
| async_tree_io_tg          | 605 ms                                                          | 627 ms: 1.04x slower                                                     |
| async_tree_none           | 218 ms                                                          | 229 ms: 1.05x slower                                                     |
| async_tree_memoization    | 264 ms                                                          | 278 ms: 1.05x slower                                                     |
| async_tree_memoization_tg | 258 ms                                                          | 274 ms: 1.06x slower                                                     |
| async_tree_none_tg        | 202 ms                                                          | 225 ms: 1.11x slower                                                     |
| Geometric mean            | (ref)                                                           | 1.05x slower                                                             |

Benchmark hidden because not significant (2): async_tree_cpu_io_mixed_tg, async_tree_io

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240605-pythonperf1-amd64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240415-pythonperf1-amd64-gvanrossum-disable_tier2-3.13.0a6+-2055e5f |
|----------------|:---------------------------------------------------------------:|:------------------------------------------------------------------------:|
| pidigits       | 150 ms                                                          | 147 ms: 1.02x faster                                                     |
| nbody          | 67.6 ms                                                         | 69.8 ms: 1.03x slower                                                    |
| float          | 49.7 ms                                                         | 53.0 ms: 1.07x slower                                                    |
| Geometric mean | (ref)                                                           | 1.02x slower                                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240605-pythonperf1-amd64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240415-pythonperf1-amd64-gvanrossum-disable_tier2-3.13.0a6+-2055e5f |
|----------------|:---------------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_effbot   | 1.58 ms                                                         | 1.57 ms: 1.01x faster                                                    |
| regex_dna      | 119 ms                                                          | 120 ms: 1.01x slower                                                     |
| regex_compile  | 78.0 ms                                                         | 80.8 ms: 1.04x slower                                                    |
| Geometric mean | (ref)                                                           | 1.00x slower                                                             |

Benchmark hidden because not significant (1): regex_v8

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240605-pythonperf1-amd64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240415-pythonperf1-amd64-gvanrossum-disable_tier2-3.13.0a6+-2055e5f |
|----------------------|:---------------------------------------------------------------:|:------------------------------------------------------------------------:|
| json_loads           | 14.2 us                                                         | 13.6 us: 1.04x faster                                                    |
| unpickle             | 8.40 us                                                         | 8.32 us: 1.01x faster                                                    |
| xml_etree_parse      | 90.9 ms                                                         | 92.3 ms: 1.02x slower                                                    |
| json_dumps           | 5.61 ms                                                         | 5.71 ms: 1.02x slower                                                    |
| xml_etree_iterparse  | 62.3 ms                                                         | 63.8 ms: 1.02x slower                                                    |
| pickle_pure_python   | 175 us                                                          | 183 us: 1.04x slower                                                     |
| unpickle_list        | 2.62 us                                                         | 2.74 us: 1.05x slower                                                    |
| pickle               | 7.11 us                                                         | 7.45 us: 1.05x slower                                                    |
| xml_etree_process    | 36.4 ms                                                         | 38.5 ms: 1.06x slower                                                    |
| tomli_loads          | 1.35 sec                                                        | 1.43 sec: 1.06x slower                                                   |
| xml_etree_generate   | 53.2 ms                                                         | 56.6 ms: 1.06x slower                                                    |
| unpickle_pure_python | 122 us                                                          | 133 us: 1.09x slower                                                     |
| pickle_dict          | 18.1 us                                                         | 19.8 us: 1.09x slower                                                    |
| pickle_list          | 2.90 us                                                         | 3.18 us: 1.10x slower                                                    |
| Geometric mean       | (ref)                                                           | 1.04x slower                                                             |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240605-pythonperf1-amd64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240415-pythonperf1-amd64-gvanrossum-disable_tier2-3.13.0a6+-2055e5f |
|------------------------|:---------------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup_no_site | 16.2 ms                                                         | 16.8 ms: 1.03x slower                                                    |
| Geometric mean         | (ref)                                                           | 1.02x slower                                                             |

Benchmark hidden because not significant (1): python_startup

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240605-pythonperf1-amd64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240415-pythonperf1-amd64-gvanrossum-disable_tier2-3.13.0a6+-2055e5f |
|-----------------|:---------------------------------------------------------------:|:------------------------------------------------------------------------:|
| django_template | 21.7 ms                                                         | 23.3 ms: 1.08x slower                                                    |
| genshi_xml      | 31.6 ms                                                         | 34.4 ms: 1.09x slower                                                    |
| genshi_text     | 14.4 ms                                                         | 16.1 ms: 1.12x slower                                                    |
| Geometric mean  | (ref)                                                           | 1.07x slower                                                             |

Benchmark hidden because not significant (1): mako

All benchmarks:
===============

| Benchmark                 | bm-20240605-pythonperf1-amd64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240415-pythonperf1-amd64-gvanrossum-disable_tier2-3.13.0a6+-2055e5f |
|---------------------------|:---------------------------------------------------------------:|:------------------------------------------------------------------------:|
| typing_runtime_protocols  | 101 us                                                          | 72.8 us: 1.39x faster                                                    |
| json_loads                | 14.2 us                                                         | 13.6 us: 1.04x faster                                                    |
| pidigits                  | 150 ms                                                          | 147 ms: 1.02x faster                                                     |
| unpickle                  | 8.40 us                                                         | 8.32 us: 1.01x faster                                                    |
| aiohttp                   | 889 us                                                          | 880 us: 1.01x faster                                                     |
| regex_effbot              | 1.58 ms                                                         | 1.57 ms: 1.01x faster                                                    |
| scimark_lu                | 56.6 ms                                                         | 56.1 ms: 1.01x faster                                                    |
| deepcopy_memo             | 22.1 us                                                         | 21.9 us: 1.01x faster                                                    |
| gc_traversal              | 1.55 ms                                                         | 1.55 ms: 1.01x faster                                                    |
| crypto_pyaes              | 45.5 ms                                                         | 45.2 ms: 1.01x faster                                                    |
| sympy_sum                 | 84.4 ms                                                         | 84.8 ms: 1.00x slower                                                    |
| regex_dna                 | 119 ms                                                          | 120 ms: 1.01x slower                                                     |
| tornado_http              | 81.8 ms                                                         | 82.6 ms: 1.01x slower                                                    |
| deepcopy                  | 220 us                                                          | 222 us: 1.01x slower                                                     |
| chaos                     | 38.4 ms                                                         | 38.8 ms: 1.01x slower                                                    |
| scimark_sor               | 75.3 ms                                                         | 76.2 ms: 1.01x slower                                                    |
| chameleon                 | 4.80 ms                                                         | 4.87 ms: 1.01x slower                                                    |
| mypy2                     | 418 ms                                                          | 424 ms: 1.02x slower                                                     |
| xml_etree_parse           | 90.9 ms                                                         | 92.3 ms: 1.02x slower                                                    |
| json_dumps                | 5.61 ms                                                         | 5.71 ms: 1.02x slower                                                    |
| docutils                  | 1.63 sec                                                        | 1.65 sec: 1.02x slower                                                   |
| deepcopy_reduce           | 1.99 us                                                         | 2.03 us: 1.02x slower                                                    |
| sympy_expand              | 271 ms                                                          | 276 ms: 1.02x slower                                                     |
| sympy_str                 | 159 ms                                                          | 162 ms: 1.02x slower                                                     |
| 2to3                      | 207 ms                                                          | 211 ms: 1.02x slower                                                     |
| xml_etree_iterparse       | 62.3 ms                                                         | 63.8 ms: 1.02x slower                                                    |
| async_tree_cpu_io_mixed   | 389 ms                                                          | 399 ms: 1.02x slower                                                     |
| comprehensions            | 10.4 us                                                         | 10.7 us: 1.03x slower                                                    |
| sympy_integrate           | 12.2 ms                                                         | 12.6 ms: 1.03x slower                                                    |
| pprint_pformat            | 966 ms                                                          | 996 ms: 1.03x slower                                                     |
| nbody                     | 67.6 ms                                                         | 69.8 ms: 1.03x slower                                                    |
| spectral_norm             | 63.7 ms                                                         | 65.8 ms: 1.03x slower                                                    |
| pprint_safe_repr          | 474 ms                                                          | 489 ms: 1.03x slower                                                     |
| python_startup_no_site    | 16.2 ms                                                         | 16.8 ms: 1.03x slower                                                    |
| raytrace                  | 162 ms                                                          | 168 ms: 1.04x slower                                                     |
| sqlglot_transpile         | 955 us                                                          | 989 us: 1.04x slower                                                     |
| async_tree_io_tg          | 605 ms                                                          | 627 ms: 1.04x slower                                                     |
| regex_compile             | 78.0 ms                                                         | 80.8 ms: 1.04x slower                                                    |
| pyflate                   | 279 ms                                                          | 289 ms: 1.04x slower                                                     |
| fannkuch                  | 243 ms                                                          | 253 ms: 1.04x slower                                                     |
| pickle_pure_python        | 175 us                                                          | 183 us: 1.04x slower                                                     |
| sqlite_synth              | 1.60 us                                                         | 1.67 us: 1.04x slower                                                    |
| logging_simple            | 5.78 us                                                         | 6.03 us: 1.04x slower                                                    |
| hexiom                    | 3.72 ms                                                         | 3.89 ms: 1.04x slower                                                    |
| bench_thread_pool         | 768 us                                                          | 803 us: 1.05x slower                                                     |
| mdp                       | 1.31 sec                                                        | 1.37 sec: 1.05x slower                                                   |
| unpickle_list             | 2.62 us                                                         | 2.74 us: 1.05x slower                                                    |
| logging_format            | 6.22 us                                                         | 6.52 us: 1.05x slower                                                    |
| pickle                    | 7.11 us                                                         | 7.45 us: 1.05x slower                                                    |
| sqlglot_optimize          | 32.7 ms                                                         | 34.3 ms: 1.05x slower                                                    |
| async_generators          | 223 ms                                                          | 234 ms: 1.05x slower                                                     |
| coroutines                | 12.8 ms                                                         | 13.4 ms: 1.05x slower                                                    |
| html5lib                  | 35.0 ms                                                         | 36.8 ms: 1.05x slower                                                    |
| async_tree_none           | 218 ms                                                          | 229 ms: 1.05x slower                                                     |
| async_tree_memoization    | 264 ms                                                          | 278 ms: 1.05x slower                                                     |
| meteor_contest            | 69.9 ms                                                         | 73.6 ms: 1.05x slower                                                    |
| sqlglot_normalize         | 173 ms                                                          | 182 ms: 1.05x slower                                                     |
| sqlglot_parse             | 748 us                                                          | 790 us: 1.06x slower                                                     |
| xml_etree_process         | 36.4 ms                                                         | 38.5 ms: 1.06x slower                                                    |
| tomli_loads               | 1.35 sec                                                        | 1.43 sec: 1.06x slower                                                   |
| nqueens                   | 56.7 ms                                                         | 60.0 ms: 1.06x slower                                                    |
| async_tree_memoization_tg | 258 ms                                                          | 274 ms: 1.06x slower                                                     |
| generators                | 19.6 ms                                                         | 20.8 ms: 1.06x slower                                                    |
| xml_etree_generate        | 53.2 ms                                                         | 56.6 ms: 1.06x slower                                                    |
| float                     | 49.7 ms                                                         | 53.0 ms: 1.07x slower                                                    |
| scimark_monte_carlo       | 39.1 ms                                                         | 41.7 ms: 1.07x slower                                                    |
| dulwich_log               | 38.0 ms                                                         | 40.6 ms: 1.07x slower                                                    |
| logging_silent            | 52.9 ns                                                         | 56.6 ns: 1.07x slower                                                    |
| django_template           | 21.7 ms                                                         | 23.3 ms: 1.08x slower                                                    |
| scimark_sparse_mat_mult   | 2.50 ms                                                         | 2.70 ms: 1.08x slower                                                    |
| telco                     | 4.67 ms                                                         | 5.05 ms: 1.08x slower                                                    |
| deltablue                 | 1.88 ms                                                         | 2.05 ms: 1.09x slower                                                    |
| genshi_xml                | 31.6 ms                                                         | 34.4 ms: 1.09x slower                                                    |
| unpickle_pure_python      | 122 us                                                          | 133 us: 1.09x slower                                                     |
| pickle_dict               | 18.1 us                                                         | 19.8 us: 1.09x slower                                                    |
| pickle_list               | 2.90 us                                                         | 3.18 us: 1.10x slower                                                    |
| scimark_fft               | 171 ms                                                          | 188 ms: 1.10x slower                                                     |
| go                        | 82.1 ms                                                         | 91.0 ms: 1.11x slower                                                    |
| async_tree_none_tg        | 202 ms                                                          | 225 ms: 1.11x slower                                                     |
| richards_super            | 30.2 ms                                                         | 33.7 ms: 1.12x slower                                                    |
| richards                  | 26.7 ms                                                         | 29.9 ms: 1.12x slower                                                    |
| genshi_text               | 14.4 ms                                                         | 16.1 ms: 1.12x slower                                                    |
| coverage                  | 42.1 ms                                                         | 47.3 ms: 1.12x slower                                                    |
| asyncio_tcp_ssl           | 1.48 sec                                                        | 1.71 sec: 1.15x slower                                                   |
| Geometric mean            | (ref)                                                           | 1.03x slower                                                             |

Benchmark hidden because not significant (13): json, pycparser, regex_v8, bench_mp_pool, thrift, create_gc_cycles, mako, python_startup, pathlib, async_tree_cpu_io_mixed_tg, pylint, asyncio_tcp, async_tree_io
Ignored benchmarks (1) of results/bm-20240605-3.13.0b2-3a83b17/bm-20240605-pythonperf1-amd64-python-v3.13.0b2-3.13.0b2-3a83b17.json: flaskblogging

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.03x
- 95% likely to have a slowdown of 1.02x
- 99% likely to have a slowdown of 1.02x

# Memory
- memory change: unknown