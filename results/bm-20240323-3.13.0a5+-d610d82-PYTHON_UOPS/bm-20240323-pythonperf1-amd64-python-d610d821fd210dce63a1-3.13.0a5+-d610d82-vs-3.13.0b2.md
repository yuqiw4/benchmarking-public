# Results vs. 3.13.0b2

- fork: python
- ref: d610d821fd210dce63a1
- machine: windows-amd64
- commit hash: d610d82
- commit date: 2024-03-23
- overall geometric mean: 1.09x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.07x slower
- Memory change: unknown

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240605-pythonperf1-amd64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240323-pythonperf1-amd64-python-d610d821fd210dce63a1-3.13.0a5+-d610d82 |
|----------------|:---------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| 2to3           | 207 ms                                                          | 225 ms: 1.09x slower                                                        |
| chameleon      | 4.80 ms                                                         | 4.89 ms: 1.02x slower                                                       |
| docutils       | 1.63 sec                                                        | 1.74 sec: 1.07x slower                                                      |
| html5lib       | 35.0 ms                                                         | 38.8 ms: 1.11x slower                                                       |
| tornado_http   | 81.8 ms                                                         | 87.1 ms: 1.06x slower                                                       |
| Geometric mean | (ref)                                                           | 1.07x slower                                                                |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                 | bm-20240605-pythonperf1-amd64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240323-pythonperf1-amd64-python-d610d821fd210dce63a1-3.13.0a5+-d610d82 |
|---------------------------|:---------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| async_tree_io_tg          | 605 ms                                                          | 564 ms: 1.07x faster                                                        |
| async_tree_none_tg        | 202 ms                                                          | 210 ms: 1.04x slower                                                        |
| async_tree_memoization    | 264 ms                                                          | 276 ms: 1.04x slower                                                        |
| async_tree_memoization_tg | 258 ms                                                          | 274 ms: 1.06x slower                                                        |
| Geometric mean            | (ref)                                                           | 1.01x slower                                                                |

Benchmark hidden because not significant (4): async_tree_cpu_io_mixed, async_tree_io, async_tree_cpu_io_mixed_tg, async_tree_none

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240605-pythonperf1-amd64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240323-pythonperf1-amd64-python-d610d821fd210dce63a1-3.13.0a5+-d610d82 |
|----------------|:---------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| pidigits       | 150 ms                                                          | 148 ms: 1.02x faster                                                        |
| float          | 49.7 ms                                                         | 57.1 ms: 1.15x slower                                                       |
| nbody          | 67.6 ms                                                         | 79.6 ms: 1.18x slower                                                       |
| Geometric mean | (ref)                                                           | 1.10x slower                                                                |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240605-pythonperf1-amd64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240323-pythonperf1-amd64-python-d610d821fd210dce63a1-3.13.0a5+-d610d82 |
|----------------|:---------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| regex_effbot   | 1.58 ms                                                         | 1.60 ms: 1.01x slower                                                       |
| regex_dna      | 119 ms                                                          | 120 ms: 1.01x slower                                                        |
| regex_compile  | 78.0 ms                                                         | 103 ms: 1.32x slower                                                        |
| Geometric mean | (ref)                                                           | 1.06x slower                                                                |

Benchmark hidden because not significant (1): regex_v8

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240605-pythonperf1-amd64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240323-pythonperf1-amd64-python-d610d821fd210dce63a1-3.13.0a5+-d610d82 |
|----------------------|:---------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| json_loads           | 14.2 us                                                         | 13.7 us: 1.03x faster                                                       |
| unpickle_list        | 2.62 us                                                         | 2.64 us: 1.01x slower                                                       |
| xml_etree_parse      | 90.9 ms                                                         | 91.9 ms: 1.01x slower                                                       |
| pickle_dict          | 18.1 us                                                         | 18.4 us: 1.01x slower                                                       |
| pickle_pure_python   | 175 us                                                          | 180 us: 1.02x slower                                                        |
| xml_etree_generate   | 53.2 ms                                                         | 55.1 ms: 1.04x slower                                                       |
| xml_etree_process    | 36.4 ms                                                         | 38.1 ms: 1.05x slower                                                       |
| xml_etree_iterparse  | 62.3 ms                                                         | 66.6 ms: 1.07x slower                                                       |
| pickle_list          | 2.90 us                                                         | 3.12 us: 1.07x slower                                                       |
| tomli_loads          | 1.35 sec                                                        | 1.50 sec: 1.11x slower                                                      |
| unpickle_pure_python | 122 us                                                          | 160 us: 1.31x slower                                                        |
| Geometric mean       | (ref)                                                           | 1.05x slower                                                                |

Benchmark hidden because not significant (3): pickle, unpickle, json_dumps

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240605-pythonperf1-amd64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240323-pythonperf1-amd64-python-d610d821fd210dce63a1-3.13.0a5+-d610d82 |
|------------------------|:---------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| python_startup_no_site | 16.2 ms                                                         | 18.0 ms: 1.11x slower                                                       |
| Geometric mean         | (ref)                                                           | 1.06x slower                                                                |

Benchmark hidden because not significant (1): python_startup

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240605-pythonperf1-amd64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240323-pythonperf1-amd64-python-d610d821fd210dce63a1-3.13.0a5+-d610d82 |
|-----------------|:---------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| django_template | 21.7 ms                                                         | 23.5 ms: 1.08x slower                                                       |
| genshi_xml      | 31.6 ms                                                         | 36.0 ms: 1.14x slower                                                       |
| mako            | 6.36 ms                                                         | 7.39 ms: 1.16x slower                                                       |
| genshi_text     | 14.4 ms                                                         | 16.9 ms: 1.17x slower                                                       |
| Geometric mean  | (ref)                                                           | 1.14x slower                                                                |

All benchmarks:
===============

| Benchmark                 | bm-20240605-pythonperf1-amd64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240323-pythonperf1-amd64-python-d610d821fd210dce63a1-3.13.0a5+-d610d82 |
|---------------------------|:---------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| typing_runtime_protocols  | 101 us                                                          | 73.5 us: 1.37x faster                                                       |
| create_gc_cycles          | 888 us                                                          | 744 us: 1.19x faster                                                        |
| json                      | 3.19 ms                                                         | 2.88 ms: 1.10x faster                                                       |
| async_tree_io_tg          | 605 ms                                                          | 564 ms: 1.07x faster                                                        |
| gc_traversal              | 1.55 ms                                                         | 1.48 ms: 1.05x faster                                                       |
| json_loads                | 14.2 us                                                         | 13.7 us: 1.03x faster                                                       |
| pidigits                  | 150 ms                                                          | 148 ms: 1.02x faster                                                        |
| unpickle_list             | 2.62 us                                                         | 2.64 us: 1.01x slower                                                       |
| deepcopy_reduce           | 1.99 us                                                         | 2.01 us: 1.01x slower                                                       |
| xml_etree_parse           | 90.9 ms                                                         | 91.9 ms: 1.01x slower                                                       |
| regex_effbot              | 1.58 ms                                                         | 1.60 ms: 1.01x slower                                                       |
| regex_dna                 | 119 ms                                                          | 120 ms: 1.01x slower                                                        |
| pickle_dict               | 18.1 us                                                         | 18.4 us: 1.01x slower                                                       |
| chameleon                 | 4.80 ms                                                         | 4.89 ms: 1.02x slower                                                       |
| sqlite_synth              | 1.60 us                                                         | 1.63 us: 1.02x slower                                                       |
| pickle_pure_python        | 175 us                                                          | 180 us: 1.02x slower                                                        |
| pathlib                   | 75.9 ms                                                         | 78.6 ms: 1.04x slower                                                       |
| xml_etree_generate        | 53.2 ms                                                         | 55.1 ms: 1.04x slower                                                       |
| aiohttp                   | 889 us                                                          | 921 us: 1.04x slower                                                        |
| telco                     | 4.67 ms                                                         | 4.85 ms: 1.04x slower                                                       |
| coroutines                | 12.8 ms                                                         | 13.2 ms: 1.04x slower                                                       |
| async_tree_none_tg        | 202 ms                                                          | 210 ms: 1.04x slower                                                        |
| async_tree_memoization    | 264 ms                                                          | 276 ms: 1.04x slower                                                        |
| xml_etree_process         | 36.4 ms                                                         | 38.1 ms: 1.05x slower                                                       |
| richards_super            | 30.2 ms                                                         | 31.7 ms: 1.05x slower                                                       |
| richards                  | 26.7 ms                                                         | 28.2 ms: 1.05x slower                                                       |
| async_tree_memoization_tg | 258 ms                                                          | 274 ms: 1.06x slower                                                        |
| deepcopy                  | 220 us                                                          | 234 us: 1.06x slower                                                        |
| deepcopy_memo             | 22.1 us                                                         | 23.5 us: 1.06x slower                                                       |
| tornado_http              | 81.8 ms                                                         | 87.1 ms: 1.06x slower                                                       |
| xml_etree_iterparse       | 62.3 ms                                                         | 66.6 ms: 1.07x slower                                                       |
| docutils                  | 1.63 sec                                                        | 1.74 sec: 1.07x slower                                                      |
| pickle_list               | 2.90 us                                                         | 3.12 us: 1.07x slower                                                       |
| pylint                    | 205 ms                                                          | 220 ms: 1.08x slower                                                        |
| logging_silent            | 52.9 ns                                                         | 57.2 ns: 1.08x slower                                                       |
| meteor_contest            | 69.9 ms                                                         | 75.6 ms: 1.08x slower                                                       |
| django_template           | 21.7 ms                                                         | 23.5 ms: 1.08x slower                                                       |
| 2to3                      | 207 ms                                                          | 225 ms: 1.09x slower                                                        |
| crypto_pyaes              | 45.5 ms                                                         | 49.6 ms: 1.09x slower                                                       |
| asyncio_tcp_ssl           | 1.48 sec                                                        | 1.62 sec: 1.09x slower                                                      |
| coverage                  | 42.1 ms                                                         | 46.1 ms: 1.10x slower                                                       |
| bench_thread_pool         | 768 us                                                          | 843 us: 1.10x slower                                                        |
| pprint_safe_repr          | 474 ms                                                          | 522 ms: 1.10x slower                                                        |
| async_generators          | 223 ms                                                          | 246 ms: 1.10x slower                                                        |
| sqlglot_parse             | 748 us                                                          | 824 us: 1.10x slower                                                        |
| logging_format            | 6.22 us                                                         | 6.86 us: 1.10x slower                                                       |
| sqlglot_normalize         | 173 ms                                                          | 191 ms: 1.10x slower                                                        |
| sqlglot_transpile         | 955 us                                                          | 1.05 ms: 1.10x slower                                                       |
| tomli_loads               | 1.35 sec                                                        | 1.50 sec: 1.11x slower                                                      |
| html5lib                  | 35.0 ms                                                         | 38.8 ms: 1.11x slower                                                       |
| python_startup_no_site    | 16.2 ms                                                         | 18.0 ms: 1.11x slower                                                       |
| logging_simple            | 5.78 us                                                         | 6.44 us: 1.11x slower                                                       |
| pprint_pformat            | 966 ms                                                          | 1.08 sec: 1.12x slower                                                      |
| generators                | 19.6 ms                                                         | 21.9 ms: 1.12x slower                                                       |
| mdp                       | 1.31 sec                                                        | 1.47 sec: 1.12x slower                                                      |
| mypy2                     | 418 ms                                                          | 470 ms: 1.13x slower                                                        |
| sympy_sum                 | 84.4 ms                                                         | 95.2 ms: 1.13x slower                                                       |
| sqlglot_optimize          | 32.7 ms                                                         | 36.9 ms: 1.13x slower                                                       |
| sympy_str                 | 159 ms                                                          | 181 ms: 1.14x slower                                                        |
| sympy_expand              | 271 ms                                                          | 308 ms: 1.14x slower                                                        |
| sympy_integrate           | 12.2 ms                                                         | 13.9 ms: 1.14x slower                                                       |
| genshi_xml                | 31.6 ms                                                         | 36.0 ms: 1.14x slower                                                       |
| fannkuch                  | 243 ms                                                          | 279 ms: 1.14x slower                                                        |
| float                     | 49.7 ms                                                         | 57.1 ms: 1.15x slower                                                       |
| mako                      | 6.36 ms                                                         | 7.39 ms: 1.16x slower                                                       |
| deltablue                 | 1.88 ms                                                         | 2.21 ms: 1.17x slower                                                       |
| chaos                     | 38.4 ms                                                         | 45.0 ms: 1.17x slower                                                       |
| thrift                    | 8.11 ms                                                         | 9.52 ms: 1.17x slower                                                       |
| genshi_text               | 14.4 ms                                                         | 16.9 ms: 1.17x slower                                                       |
| dulwich_log               | 38.0 ms                                                         | 44.8 ms: 1.18x slower                                                       |
| nbody                     | 67.6 ms                                                         | 79.6 ms: 1.18x slower                                                       |
| scimark_sor               | 75.3 ms                                                         | 89.2 ms: 1.18x slower                                                       |
| raytrace                  | 162 ms                                                          | 194 ms: 1.20x slower                                                        |
| pyflate                   | 279 ms                                                          | 339 ms: 1.22x slower                                                        |
| nqueens                   | 56.7 ms                                                         | 69.5 ms: 1.23x slower                                                       |
| go                        | 82.1 ms                                                         | 101 ms: 1.23x slower                                                        |
| scimark_fft               | 171 ms                                                          | 212 ms: 1.24x slower                                                        |
| spectral_norm             | 63.7 ms                                                         | 82.7 ms: 1.30x slower                                                       |
| comprehensions            | 10.4 us                                                         | 13.5 us: 1.30x slower                                                       |
| scimark_monte_carlo       | 39.1 ms                                                         | 51.2 ms: 1.31x slower                                                       |
| unpickle_pure_python      | 122 us                                                          | 160 us: 1.31x slower                                                        |
| scimark_sparse_mat_mult   | 2.50 ms                                                         | 3.29 ms: 1.32x slower                                                       |
| regex_compile             | 78.0 ms                                                         | 103 ms: 1.32x slower                                                        |
| scimark_lu                | 56.6 ms                                                         | 78.1 ms: 1.38x slower                                                       |
| hexiom                    | 3.72 ms                                                         | 5.35 ms: 1.44x slower                                                       |
| Geometric mean            | (ref)                                                           | 1.09x slower                                                                |

Benchmark hidden because not significant (12): regex_v8, pycparser, async_tree_cpu_io_mixed, async_tree_io, pickle, async_tree_cpu_io_mixed_tg, unpickle, json_dumps, bench_mp_pool, python_startup, async_tree_none, asyncio_tcp
Ignored benchmarks (1) of results/bm-20240605-3.13.0b2-3a83b17/bm-20240605-pythonperf1-amd64-python-v3.13.0b2-3.13.0b2-3a83b17.json: flaskblogging
Ignored benchmarks (1) of results/bm-20240323-3.13.0a5+-d610d82-PYTHON_UOPS/bm-20240323-pythonperf1-amd64-python-d610d821fd210dce63a1-3.13.0a5+-d610d82.json: unpack_sequence

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.08x
- 95% likely to have a slowdown of 1.08x
- 99% likely to have a slowdown of 1.07x

# Memory
- memory change: unknown