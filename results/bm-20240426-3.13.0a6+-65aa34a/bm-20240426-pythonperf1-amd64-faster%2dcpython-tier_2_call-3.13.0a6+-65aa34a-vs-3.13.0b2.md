# Results vs. 3.13.0b2

- fork: faster-cpython
- ref: tier_2_call
- machine: windows-amd64
- commit hash: 65aa34a
- commit date: 2024-04-26
- overall geometric mean: 1.05x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.03x slower
- Memory change: unknown

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240605-pythonperf1-amd64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240426-pythonperf1-amd64-faster%2dcpython-tier_2_call-3.13.0a6+-65aa34a |
|----------------|:---------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| 2to3           | 207 ms                                                          | 217 ms: 1.05x slower                                                         |
| chameleon      | 4.80 ms                                                         | 5.05 ms: 1.05x slower                                                        |
| docutils       | 1.63 sec                                                        | 1.65 sec: 1.02x slower                                                       |
| html5lib       | 35.0 ms                                                         | 36.5 ms: 1.04x slower                                                        |
| tornado_http   | 81.8 ms                                                         | 90.9 ms: 1.11x slower                                                        |
| Geometric mean | (ref)                                                           | 1.05x slower                                                                 |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                 | bm-20240605-pythonperf1-amd64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240426-pythonperf1-amd64-faster%2dcpython-tier_2_call-3.13.0a6+-65aa34a |
|---------------------------|:---------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| async_tree_cpu_io_mixed   | 389 ms                                                          | 402 ms: 1.03x slower                                                         |
| async_tree_io             | 588 ms                                                          | 612 ms: 1.04x slower                                                         |
| async_tree_io_tg          | 605 ms                                                          | 635 ms: 1.05x slower                                                         |
| async_tree_memoization    | 264 ms                                                          | 282 ms: 1.07x slower                                                         |
| async_tree_none           | 218 ms                                                          | 233 ms: 1.07x slower                                                         |
| async_tree_memoization_tg | 258 ms                                                          | 280 ms: 1.08x slower                                                         |
| async_tree_none_tg        | 202 ms                                                          | 224 ms: 1.11x slower                                                         |
| Geometric mean            | (ref)                                                           | 1.06x slower                                                                 |

Benchmark hidden because not significant (1): async_tree_cpu_io_mixed_tg

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240605-pythonperf1-amd64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240426-pythonperf1-amd64-faster%2dcpython-tier_2_call-3.13.0a6+-65aa34a |
|----------------|:---------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| pidigits       | 150 ms                                                          | 149 ms: 1.01x faster                                                         |
| float          | 49.7 ms                                                         | 51.5 ms: 1.04x slower                                                        |
| nbody          | 67.6 ms                                                         | 72.9 ms: 1.08x slower                                                        |
| Geometric mean | (ref)                                                           | 1.03x slower                                                                 |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240605-pythonperf1-amd64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240426-pythonperf1-amd64-faster%2dcpython-tier_2_call-3.13.0a6+-65aa34a |
|----------------|:---------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| regex_v8       | 15.8 ms                                                         | 14.6 ms: 1.08x faster                                                        |
| regex_dna      | 119 ms                                                          | 114 ms: 1.04x faster                                                         |
| regex_effbot   | 1.58 ms                                                         | 1.57 ms: 1.01x faster                                                        |
| regex_compile  | 78.0 ms                                                         | 79.4 ms: 1.02x slower                                                        |
| Geometric mean | (ref)                                                           | 1.03x faster                                                                 |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240605-pythonperf1-amd64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240426-pythonperf1-amd64-faster%2dcpython-tier_2_call-3.13.0a6+-65aa34a |
|----------------------|:---------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| json_loads           | 14.2 us                                                         | 13.7 us: 1.04x faster                                                        |
| pickle_pure_python   | 175 us                                                          | 176 us: 1.00x slower                                                         |
| pickle_dict          | 18.1 us                                                         | 18.4 us: 1.01x slower                                                        |
| xml_etree_parse      | 90.9 ms                                                         | 92.3 ms: 1.01x slower                                                        |
| unpickle             | 8.40 us                                                         | 8.57 us: 1.02x slower                                                        |
| pickle               | 7.11 us                                                         | 7.27 us: 1.02x slower                                                        |
| xml_etree_process    | 36.4 ms                                                         | 37.6 ms: 1.03x slower                                                        |
| xml_etree_iterparse  | 62.3 ms                                                         | 64.7 ms: 1.04x slower                                                        |
| json_dumps           | 5.61 ms                                                         | 5.83 ms: 1.04x slower                                                        |
| xml_etree_generate   | 53.2 ms                                                         | 55.2 ms: 1.04x slower                                                        |
| unpickle_list        | 2.62 us                                                         | 2.78 us: 1.06x slower                                                        |
| pickle_list          | 2.90 us                                                         | 3.11 us: 1.07x slower                                                        |
| tomli_loads          | 1.35 sec                                                        | 1.45 sec: 1.07x slower                                                       |
| unpickle_pure_python | 122 us                                                          | 133 us: 1.09x slower                                                         |
| Geometric mean       | (ref)                                                           | 1.03x slower                                                                 |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240605-pythonperf1-amd64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240426-pythonperf1-amd64-faster%2dcpython-tier_2_call-3.13.0a6+-65aa34a |
|------------------------|:---------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| python_startup         | 20.3 ms                                                         | 20.6 ms: 1.02x slower                                                        |
| python_startup_no_site | 16.2 ms                                                         | 16.7 ms: 1.03x slower                                                        |
| Geometric mean         | (ref)                                                           | 1.02x slower                                                                 |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240605-pythonperf1-amd64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240426-pythonperf1-amd64-faster%2dcpython-tier_2_call-3.13.0a6+-65aa34a |
|-----------------|:---------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| django_template | 21.7 ms                                                         | 22.4 ms: 1.03x slower                                                        |
| genshi_xml      | 31.6 ms                                                         | 34.4 ms: 1.09x slower                                                        |
| genshi_text     | 14.4 ms                                                         | 16.2 ms: 1.13x slower                                                        |
| Geometric mean  | (ref)                                                           | 1.06x slower                                                                 |

Benchmark hidden because not significant (1): mako

All benchmarks:
===============

| Benchmark                 | bm-20240605-pythonperf1-amd64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240426-pythonperf1-amd64-faster%2dcpython-tier_2_call-3.13.0a6+-65aa34a |
|---------------------------|:---------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| regex_v8                  | 15.8 ms                                                         | 14.6 ms: 1.08x faster                                                        |
| regex_dna                 | 119 ms                                                          | 114 ms: 1.04x faster                                                         |
| json_loads                | 14.2 us                                                         | 13.7 us: 1.04x faster                                                        |
| regex_effbot              | 1.58 ms                                                         | 1.57 ms: 1.01x faster                                                        |
| pidigits                  | 150 ms                                                          | 149 ms: 1.01x faster                                                         |
| pickle_pure_python        | 175 us                                                          | 176 us: 1.00x slower                                                         |
| deepcopy                  | 220 us                                                          | 221 us: 1.01x slower                                                         |
| bench_mp_pool             | 64.8 ms                                                         | 65.6 ms: 1.01x slower                                                        |
| sympy_expand              | 271 ms                                                          | 274 ms: 1.01x slower                                                         |
| create_gc_cycles          | 888 us                                                          | 901 us: 1.01x slower                                                         |
| pickle_dict               | 18.1 us                                                         | 18.4 us: 1.01x slower                                                        |
| xml_etree_parse           | 90.9 ms                                                         | 92.3 ms: 1.01x slower                                                        |
| sympy_sum                 | 84.4 ms                                                         | 85.7 ms: 1.02x slower                                                        |
| docutils                  | 1.63 sec                                                        | 1.65 sec: 1.02x slower                                                       |
| python_startup            | 20.3 ms                                                         | 20.6 ms: 1.02x slower                                                        |
| sympy_str                 | 159 ms                                                          | 162 ms: 1.02x slower                                                         |
| regex_compile             | 78.0 ms                                                         | 79.4 ms: 1.02x slower                                                        |
| chaos                     | 38.4 ms                                                         | 39.1 ms: 1.02x slower                                                        |
| unpickle                  | 8.40 us                                                         | 8.57 us: 1.02x slower                                                        |
| pickle                    | 7.11 us                                                         | 7.27 us: 1.02x slower                                                        |
| sympy_integrate           | 12.2 ms                                                         | 12.5 ms: 1.02x slower                                                        |
| raytrace                  | 162 ms                                                          | 166 ms: 1.02x slower                                                         |
| mypy2                     | 418 ms                                                          | 428 ms: 1.02x slower                                                         |
| spectral_norm             | 63.7 ms                                                         | 65.5 ms: 1.03x slower                                                        |
| scimark_lu                | 56.6 ms                                                         | 58.1 ms: 1.03x slower                                                        |
| deepcopy_reduce           | 1.99 us                                                         | 2.05 us: 1.03x slower                                                        |
| coroutines                | 12.8 ms                                                         | 13.1 ms: 1.03x slower                                                        |
| scimark_sor               | 75.3 ms                                                         | 77.7 ms: 1.03x slower                                                        |
| python_startup_no_site    | 16.2 ms                                                         | 16.7 ms: 1.03x slower                                                        |
| async_tree_cpu_io_mixed   | 389 ms                                                          | 402 ms: 1.03x slower                                                         |
| xml_etree_process         | 36.4 ms                                                         | 37.6 ms: 1.03x slower                                                        |
| django_template           | 21.7 ms                                                         | 22.4 ms: 1.03x slower                                                        |
| pyflate                   | 279 ms                                                          | 288 ms: 1.03x slower                                                         |
| pprint_pformat            | 966 ms                                                          | 999 ms: 1.03x slower                                                         |
| deepcopy_memo             | 22.1 us                                                         | 22.9 us: 1.03x slower                                                        |
| telco                     | 4.67 ms                                                         | 4.83 ms: 1.03x slower                                                        |
| comprehensions            | 10.4 us                                                         | 10.7 us: 1.04x slower                                                        |
| float                     | 49.7 ms                                                         | 51.5 ms: 1.04x slower                                                        |
| logging_silent            | 52.9 ns                                                         | 54.9 ns: 1.04x slower                                                        |
| pprint_safe_repr          | 474 ms                                                          | 492 ms: 1.04x slower                                                         |
| xml_etree_iterparse       | 62.3 ms                                                         | 64.7 ms: 1.04x slower                                                        |
| json_dumps                | 5.61 ms                                                         | 5.83 ms: 1.04x slower                                                        |
| xml_etree_generate        | 53.2 ms                                                         | 55.2 ms: 1.04x slower                                                        |
| thrift                    | 8.11 ms                                                         | 8.42 ms: 1.04x slower                                                        |
| sqlglot_transpile         | 955 us                                                          | 994 us: 1.04x slower                                                         |
| async_tree_io             | 588 ms                                                          | 612 ms: 1.04x slower                                                         |
| html5lib                  | 35.0 ms                                                         | 36.5 ms: 1.04x slower                                                        |
| sqlite_synth              | 1.60 us                                                         | 1.67 us: 1.04x slower                                                        |
| hexiom                    | 3.72 ms                                                         | 3.88 ms: 1.04x slower                                                        |
| sqlglot_parse             | 748 us                                                          | 781 us: 1.04x slower                                                         |
| sqlglot_optimize          | 32.7 ms                                                         | 34.2 ms: 1.04x slower                                                        |
| sqlglot_normalize         | 173 ms                                                          | 181 ms: 1.05x slower                                                         |
| logging_simple            | 5.78 us                                                         | 6.05 us: 1.05x slower                                                        |
| async_tree_io_tg          | 605 ms                                                          | 635 ms: 1.05x slower                                                         |
| dulwich_log               | 38.0 ms                                                         | 39.9 ms: 1.05x slower                                                        |
| logging_format            | 6.22 us                                                         | 6.53 us: 1.05x slower                                                        |
| 2to3                      | 207 ms                                                          | 217 ms: 1.05x slower                                                         |
| aiohttp                   | 889 us                                                          | 933 us: 1.05x slower                                                         |
| chameleon                 | 4.80 ms                                                         | 5.05 ms: 1.05x slower                                                        |
| unpickle_list             | 2.62 us                                                         | 2.78 us: 1.06x slower                                                        |
| fannkuch                  | 243 ms                                                          | 259 ms: 1.07x slower                                                         |
| async_tree_memoization    | 264 ms                                                          | 282 ms: 1.07x slower                                                         |
| async_tree_none           | 218 ms                                                          | 233 ms: 1.07x slower                                                         |
| meteor_contest            | 69.9 ms                                                         | 74.8 ms: 1.07x slower                                                        |
| nqueens                   | 56.7 ms                                                         | 60.6 ms: 1.07x slower                                                        |
| pickle_list               | 2.90 us                                                         | 3.11 us: 1.07x slower                                                        |
| tomli_loads               | 1.35 sec                                                        | 1.45 sec: 1.07x slower                                                       |
| typing_runtime_protocols  | 101 us                                                          | 109 us: 1.08x slower                                                         |
| richards_super            | 30.2 ms                                                         | 32.4 ms: 1.08x slower                                                        |
| richards                  | 26.7 ms                                                         | 28.7 ms: 1.08x slower                                                        |
| nbody                     | 67.6 ms                                                         | 72.9 ms: 1.08x slower                                                        |
| async_tree_memoization_tg | 258 ms                                                          | 280 ms: 1.08x slower                                                         |
| async_generators          | 223 ms                                                          | 242 ms: 1.08x slower                                                         |
| pathlib                   | 75.9 ms                                                         | 82.3 ms: 1.08x slower                                                        |
| mdp                       | 1.31 sec                                                        | 1.43 sec: 1.09x slower                                                       |
| deltablue                 | 1.88 ms                                                         | 2.05 ms: 1.09x slower                                                        |
| genshi_xml                | 31.6 ms                                                         | 34.4 ms: 1.09x slower                                                        |
| unpickle_pure_python      | 122 us                                                          | 133 us: 1.09x slower                                                         |
| scimark_monte_carlo       | 39.1 ms                                                         | 42.8 ms: 1.09x slower                                                        |
| bench_thread_pool         | 768 us                                                          | 843 us: 1.10x slower                                                         |
| go                        | 82.1 ms                                                         | 90.7 ms: 1.11x slower                                                        |
| async_tree_none_tg        | 202 ms                                                          | 224 ms: 1.11x slower                                                         |
| tornado_http              | 81.8 ms                                                         | 90.9 ms: 1.11x slower                                                        |
| genshi_text               | 14.4 ms                                                         | 16.2 ms: 1.13x slower                                                        |
| generators                | 19.6 ms                                                         | 22.3 ms: 1.14x slower                                                        |
| scimark_sparse_mat_mult   | 2.50 ms                                                         | 2.88 ms: 1.15x slower                                                        |
| scimark_fft               | 171 ms                                                          | 197 ms: 1.15x slower                                                         |
| coverage                  | 42.1 ms                                                         | 50.6 ms: 1.20x slower                                                        |
| asyncio_tcp_ssl           | 1.48 sec                                                        | 1.84 sec: 1.24x slower                                                       |
| asyncio_tcp               | 471 ms                                                          | 664 ms: 1.41x slower                                                         |
| Geometric mean            | (ref)                                                           | 1.05x slower                                                                 |

Benchmark hidden because not significant (7): json, pycparser, crypto_pyaes, mako, gc_traversal, async_tree_cpu_io_mixed_tg, pylint
Ignored benchmarks (1) of results/bm-20240605-3.13.0b2-3a83b17/bm-20240605-pythonperf1-amd64-python-v3.13.0b2-3.13.0b2-3a83b17.json: flaskblogging

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.03x
- 95% likely to have a slowdown of 1.03x
- 99% likely to have a slowdown of 1.03x

# Memory
- memory change: unknown