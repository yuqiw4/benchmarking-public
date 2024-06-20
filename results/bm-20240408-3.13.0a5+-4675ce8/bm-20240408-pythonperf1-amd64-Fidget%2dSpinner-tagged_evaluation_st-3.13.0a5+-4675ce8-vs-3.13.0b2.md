# Results vs. 3.13.0b2

- fork: Fidget-Spinner
- ref: tagged_evaluation_st
- machine: windows-amd64
- commit hash: 4675ce8
- commit date: 2024-04-08
- overall geometric mean: 1.07x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.05x slower
- Memory change: unknown

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240605-pythonperf1-amd64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240408-pythonperf1-amd64-Fidget%2dSpinner-tagged_evaluation_st-3.13.0a5+-4675ce8 |
|----------------|:---------------------------------------------------------------:|:-------------------------------------------------------------------------------------:|
| 2to3           | 207 ms                                                          | 220 ms: 1.07x slower                                                                  |
| chameleon      | 4.80 ms                                                         | 5.55 ms: 1.16x slower                                                                 |
| docutils       | 1.63 sec                                                        | 1.70 sec: 1.05x slower                                                                |
| html5lib       | 35.0 ms                                                         | 38.0 ms: 1.09x slower                                                                 |
| tornado_http   | 81.8 ms                                                         | 84.1 ms: 1.03x slower                                                                 |
| Geometric mean | (ref)                                                           | 1.08x slower                                                                          |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                 | bm-20240605-pythonperf1-amd64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240408-pythonperf1-amd64-Fidget%2dSpinner-tagged_evaluation_st-3.13.0a5+-4675ce8 |
|---------------------------|:---------------------------------------------------------------:|:-------------------------------------------------------------------------------------:|
| async_tree_cpu_io_mixed   | 389 ms                                                          | 403 ms: 1.04x slower                                                                  |
| async_tree_io_tg          | 605 ms                                                          | 631 ms: 1.04x slower                                                                  |
| async_tree_none           | 218 ms                                                          | 232 ms: 1.07x slower                                                                  |
| async_tree_memoization    | 264 ms                                                          | 281 ms: 1.07x slower                                                                  |
| async_tree_memoization_tg | 258 ms                                                          | 280 ms: 1.08x slower                                                                  |
| async_tree_none_tg        | 202 ms                                                          | 229 ms: 1.13x slower                                                                  |
| Geometric mean            | (ref)                                                           | 1.05x slower                                                                          |

Benchmark hidden because not significant (2): async_tree_io, async_tree_cpu_io_mixed_tg

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240605-pythonperf1-amd64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240408-pythonperf1-amd64-Fidget%2dSpinner-tagged_evaluation_st-3.13.0a5+-4675ce8 |
|----------------|:---------------------------------------------------------------:|:-------------------------------------------------------------------------------------:|
| pidigits       | 150 ms                                                          | 147 ms: 1.02x faster                                                                  |
| float          | 49.7 ms                                                         | 53.0 ms: 1.07x slower                                                                 |
| nbody          | 67.6 ms                                                         | 76.0 ms: 1.12x slower                                                                 |
| Geometric mean | (ref)                                                           | 1.06x slower                                                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240605-pythonperf1-amd64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240408-pythonperf1-amd64-Fidget%2dSpinner-tagged_evaluation_st-3.13.0a5+-4675ce8 |
|----------------|:---------------------------------------------------------------:|:-------------------------------------------------------------------------------------:|
| regex_effbot   | 1.58 ms                                                         | 1.57 ms: 1.01x faster                                                                 |
| regex_compile  | 78.0 ms                                                         | 82.6 ms: 1.06x slower                                                                 |
| regex_v8       | 15.8 ms                                                         | 18.0 ms: 1.14x slower                                                                 |
| Geometric mean | (ref)                                                           | 1.05x slower                                                                          |

Benchmark hidden because not significant (1): regex_dna

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240605-pythonperf1-amd64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240408-pythonperf1-amd64-Fidget%2dSpinner-tagged_evaluation_st-3.13.0a5+-4675ce8 |
|----------------------|:---------------------------------------------------------------:|:-------------------------------------------------------------------------------------:|
| json_loads           | 14.2 us                                                         | 13.9 us: 1.02x faster                                                                 |
| unpickle             | 8.40 us                                                         | 8.48 us: 1.01x slower                                                                 |
| pickle_list          | 2.90 us                                                         | 3.00 us: 1.03x slower                                                                 |
| pickle               | 7.11 us                                                         | 7.35 us: 1.03x slower                                                                 |
| xml_etree_iterparse  | 62.3 ms                                                         | 64.6 ms: 1.04x slower                                                                 |
| pickle_dict          | 18.1 us                                                         | 18.9 us: 1.04x slower                                                                 |
| tomli_loads          | 1.35 sec                                                        | 1.45 sec: 1.07x slower                                                                |
| json_dumps           | 5.61 ms                                                         | 6.07 ms: 1.08x slower                                                                 |
| unpickle_list        | 2.62 us                                                         | 2.85 us: 1.09x slower                                                                 |
| xml_etree_generate   | 53.2 ms                                                         | 59.0 ms: 1.11x slower                                                                 |
| unpickle_pure_python | 122 us                                                          | 139 us: 1.14x slower                                                                  |
| xml_etree_process    | 36.4 ms                                                         | 41.7 ms: 1.15x slower                                                                 |
| pickle_pure_python   | 175 us                                                          | 206 us: 1.18x slower                                                                  |
| Geometric mean       | (ref)                                                           | 1.07x slower                                                                          |

Benchmark hidden because not significant (1): xml_etree_parse

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240605-pythonperf1-amd64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240408-pythonperf1-amd64-Fidget%2dSpinner-tagged_evaluation_st-3.13.0a5+-4675ce8 |
|------------------------|:---------------------------------------------------------------:|:-------------------------------------------------------------------------------------:|
| python_startup         | 20.3 ms                                                         | 20.1 ms: 1.01x faster                                                                 |
| python_startup_no_site | 16.2 ms                                                         | 17.9 ms: 1.10x slower                                                                 |
| Geometric mean         | (ref)                                                           | 1.05x slower                                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark      | bm-20240605-pythonperf1-amd64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240408-pythonperf1-amd64-Fidget%2dSpinner-tagged_evaluation_st-3.13.0a5+-4675ce8 |
|----------------|:---------------------------------------------------------------:|:-------------------------------------------------------------------------------------:|
| mako           | 6.36 ms                                                         | 6.46 ms: 1.02x slower                                                                 |
| genshi_xml     | 31.6 ms                                                         | 37.7 ms: 1.19x slower                                                                 |
| genshi_text    | 14.4 ms                                                         | 17.9 ms: 1.25x slower                                                                 |
| Geometric mean | (ref)                                                           | 1.15x slower                                                                          |

All benchmarks:
===============

| Benchmark                 | bm-20240605-pythonperf1-amd64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240408-pythonperf1-amd64-Fidget%2dSpinner-tagged_evaluation_st-3.13.0a5+-4675ce8 |
|---------------------------|:---------------------------------------------------------------:|:-------------------------------------------------------------------------------------:|
| typing_runtime_protocols  | 101 us                                                          | 75.9 us: 1.33x faster                                                                 |
| pylint                    | 205 ms                                                          | 193 ms: 1.06x faster                                                                  |
| json                      | 3.19 ms                                                         | 3.02 ms: 1.06x faster                                                                 |
| json_loads                | 14.2 us                                                         | 13.9 us: 1.02x faster                                                                 |
| pidigits                  | 150 ms                                                          | 147 ms: 1.02x faster                                                                  |
| gc_traversal              | 1.55 ms                                                         | 1.53 ms: 1.01x faster                                                                 |
| regex_effbot              | 1.58 ms                                                         | 1.57 ms: 1.01x faster                                                                 |
| python_startup            | 20.3 ms                                                         | 20.1 ms: 1.01x faster                                                                 |
| spectral_norm             | 63.7 ms                                                         | 63.3 ms: 1.01x faster                                                                 |
| unpickle                  | 8.40 us                                                         | 8.48 us: 1.01x slower                                                                 |
| aiohttp                   | 889 us                                                          | 901 us: 1.01x slower                                                                  |
| mako                      | 6.36 ms                                                         | 6.46 ms: 1.02x slower                                                                 |
| richards_super            | 30.2 ms                                                         | 30.9 ms: 1.03x slower                                                                 |
| tornado_http              | 81.8 ms                                                         | 84.1 ms: 1.03x slower                                                                 |
| richards                  | 26.7 ms                                                         | 27.5 ms: 1.03x slower                                                                 |
| pathlib                   | 75.9 ms                                                         | 78.2 ms: 1.03x slower                                                                 |
| pickle_list               | 2.90 us                                                         | 3.00 us: 1.03x slower                                                                 |
| pickle                    | 7.11 us                                                         | 7.35 us: 1.03x slower                                                                 |
| async_tree_cpu_io_mixed   | 389 ms                                                          | 403 ms: 1.04x slower                                                                  |
| xml_etree_iterparse       | 62.3 ms                                                         | 64.6 ms: 1.04x slower                                                                 |
| deepcopy_memo             | 22.1 us                                                         | 22.9 us: 1.04x slower                                                                 |
| pickle_dict               | 18.1 us                                                         | 18.9 us: 1.04x slower                                                                 |
| mypy2                     | 418 ms                                                          | 435 ms: 1.04x slower                                                                  |
| async_tree_io_tg          | 605 ms                                                          | 631 ms: 1.04x slower                                                                  |
| docutils                  | 1.63 sec                                                        | 1.70 sec: 1.05x slower                                                                |
| logging_silent            | 52.9 ns                                                         | 55.7 ns: 1.05x slower                                                                 |
| sympy_sum                 | 84.4 ms                                                         | 88.8 ms: 1.05x slower                                                                 |
| scimark_lu                | 56.6 ms                                                         | 59.6 ms: 1.05x slower                                                                 |
| scimark_sor               | 75.3 ms                                                         | 79.5 ms: 1.06x slower                                                                 |
| sympy_integrate           | 12.2 ms                                                         | 12.9 ms: 1.06x slower                                                                 |
| regex_compile             | 78.0 ms                                                         | 82.6 ms: 1.06x slower                                                                 |
| sympy_expand              | 271 ms                                                          | 287 ms: 1.06x slower                                                                  |
| async_generators          | 223 ms                                                          | 238 ms: 1.06x slower                                                                  |
| float                     | 49.7 ms                                                         | 53.0 ms: 1.07x slower                                                                 |
| async_tree_none           | 218 ms                                                          | 232 ms: 1.07x slower                                                                  |
| 2to3                      | 207 ms                                                          | 220 ms: 1.07x slower                                                                  |
| async_tree_memoization    | 264 ms                                                          | 281 ms: 1.07x slower                                                                  |
| sqlite_synth              | 1.60 us                                                         | 1.71 us: 1.07x slower                                                                 |
| scimark_fft               | 171 ms                                                          | 183 ms: 1.07x slower                                                                  |
| sympy_str                 | 159 ms                                                          | 170 ms: 1.07x slower                                                                  |
| bench_thread_pool         | 768 us                                                          | 822 us: 1.07x slower                                                                  |
| deepcopy                  | 220 us                                                          | 235 us: 1.07x slower                                                                  |
| tomli_loads               | 1.35 sec                                                        | 1.45 sec: 1.07x slower                                                                |
| scimark_sparse_mat_mult   | 2.50 ms                                                         | 2.68 ms: 1.07x slower                                                                 |
| scimark_monte_carlo       | 39.1 ms                                                         | 41.9 ms: 1.07x slower                                                                 |
| logging_format            | 6.22 us                                                         | 6.67 us: 1.07x slower                                                                 |
| go                        | 82.1 ms                                                         | 88.0 ms: 1.07x slower                                                                 |
| raytrace                  | 162 ms                                                          | 174 ms: 1.07x slower                                                                  |
| pyflate                   | 279 ms                                                          | 299 ms: 1.07x slower                                                                  |
| sqlglot_transpile         | 955 us                                                          | 1.03 ms: 1.08x slower                                                                 |
| logging_simple            | 5.78 us                                                         | 6.24 us: 1.08x slower                                                                 |
| crypto_pyaes              | 45.5 ms                                                         | 49.1 ms: 1.08x slower                                                                 |
| json_dumps                | 5.61 ms                                                         | 6.07 ms: 1.08x slower                                                                 |
| thrift                    | 8.11 ms                                                         | 8.77 ms: 1.08x slower                                                                 |
| async_tree_memoization_tg | 258 ms                                                          | 280 ms: 1.08x slower                                                                  |
| sqlglot_parse             | 748 us                                                          | 811 us: 1.08x slower                                                                  |
| html5lib                  | 35.0 ms                                                         | 38.0 ms: 1.09x slower                                                                 |
| unpickle_list             | 2.62 us                                                         | 2.85 us: 1.09x slower                                                                 |
| deltablue                 | 1.88 ms                                                         | 2.05 ms: 1.09x slower                                                                 |
| hexiom                    | 3.72 ms                                                         | 4.07 ms: 1.09x slower                                                                 |
| deepcopy_reduce           | 1.99 us                                                         | 2.18 us: 1.09x slower                                                                 |
| meteor_contest            | 69.9 ms                                                         | 76.5 ms: 1.10x slower                                                                 |
| sqlglot_optimize          | 32.7 ms                                                         | 35.9 ms: 1.10x slower                                                                 |
| chaos                     | 38.4 ms                                                         | 42.1 ms: 1.10x slower                                                                 |
| sqlglot_normalize         | 173 ms                                                          | 191 ms: 1.10x slower                                                                  |
| python_startup_no_site    | 16.2 ms                                                         | 17.9 ms: 1.10x slower                                                                 |
| xml_etree_generate        | 53.2 ms                                                         | 59.0 ms: 1.11x slower                                                                 |
| mdp                       | 1.31 sec                                                        | 1.47 sec: 1.12x slower                                                                |
| dulwich_log               | 38.0 ms                                                         | 42.6 ms: 1.12x slower                                                                 |
| nbody                     | 67.6 ms                                                         | 76.0 ms: 1.12x slower                                                                 |
| async_tree_none_tg        | 202 ms                                                          | 229 ms: 1.13x slower                                                                  |
| coverage                  | 42.1 ms                                                         | 47.7 ms: 1.13x slower                                                                 |
| regex_v8                  | 15.8 ms                                                         | 18.0 ms: 1.14x slower                                                                 |
| unpickle_pure_python      | 122 us                                                          | 139 us: 1.14x slower                                                                  |
| xml_etree_process         | 36.4 ms                                                         | 41.7 ms: 1.15x slower                                                                 |
| pprint_safe_repr          | 474 ms                                                          | 544 ms: 1.15x slower                                                                  |
| pprint_pformat            | 966 ms                                                          | 1.11 sec: 1.15x slower                                                                |
| chameleon                 | 4.80 ms                                                         | 5.55 ms: 1.16x slower                                                                 |
| telco                     | 4.67 ms                                                         | 5.40 ms: 1.16x slower                                                                 |
| asyncio_tcp_ssl           | 1.48 sec                                                        | 1.72 sec: 1.16x slower                                                                |
| nqueens                   | 56.7 ms                                                         | 66.3 ms: 1.17x slower                                                                 |
| pickle_pure_python        | 175 us                                                          | 206 us: 1.18x slower                                                                  |
| comprehensions            | 10.4 us                                                         | 12.2 us: 1.18x slower                                                                 |
| coroutines                | 12.8 ms                                                         | 15.2 ms: 1.19x slower                                                                 |
| genshi_xml                | 31.6 ms                                                         | 37.7 ms: 1.19x slower                                                                 |
| generators                | 19.6 ms                                                         | 23.4 ms: 1.19x slower                                                                 |
| fannkuch                  | 243 ms                                                          | 297 ms: 1.22x slower                                                                  |
| genshi_text               | 14.4 ms                                                         | 17.9 ms: 1.25x slower                                                                 |
| Geometric mean            | (ref)                                                           | 1.07x slower                                                                          |

Benchmark hidden because not significant (8): pycparser, async_tree_io, bench_mp_pool, create_gc_cycles, xml_etree_parse, regex_dna, asyncio_tcp, async_tree_cpu_io_mixed_tg
Ignored benchmarks (2) of results/bm-20240605-3.13.0b2-3a83b17/bm-20240605-pythonperf1-amd64-python-v3.13.0b2-3.13.0b2-3a83b17.json: django_template, flaskblogging

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.06x
- 95% likely to have a slowdown of 1.06x
- 99% likely to have a slowdown of 1.05x

# Memory
- memory change: unknown