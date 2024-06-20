# Results vs. 3.13.0b2

- fork: faster-cpython
- ref: call_cmethod
- machine: windows-amd64
- commit hash: e985127
- commit date: 2024-04-10
- overall geometric mean: 1.03x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.02x slower
- Memory change: unknown

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240605-pythonperf1-amd64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240410-pythonperf1-amd64-faster%2dcpython-call_cmethod-3.13.0a5+-e985127 |
|----------------|:---------------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| 2to3           | 207 ms                                                          | 212 ms: 1.03x slower                                                          |
| chameleon      | 4.80 ms                                                         | 4.84 ms: 1.01x slower                                                         |
| html5lib       | 35.0 ms                                                         | 35.8 ms: 1.02x slower                                                         |
| Geometric mean | (ref)                                                           | 1.01x slower                                                                  |

Benchmark hidden because not significant (2): docutils, tornado_http

Benchmarks with tag 'asyncio':
==============================

| Benchmark          | bm-20240605-pythonperf1-amd64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240410-pythonperf1-amd64-faster%2dcpython-call_cmethod-3.13.0a5+-e985127 |
|--------------------|:---------------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| async_tree_io_tg   | 605 ms                                                          | 617 ms: 1.02x slower                                                          |
| async_tree_none    | 218 ms                                                          | 223 ms: 1.02x slower                                                          |
| async_tree_none_tg | 202 ms                                                          | 218 ms: 1.08x slower                                                          |
| Geometric mean     | (ref)                                                           | 1.02x slower                                                                  |

Benchmark hidden because not significant (5): async_tree_cpu_io_mixed, async_tree_cpu_io_mixed_tg, async_tree_io, async_tree_memoization, async_tree_memoization_tg

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240605-pythonperf1-amd64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240410-pythonperf1-amd64-faster%2dcpython-call_cmethod-3.13.0a5+-e985127 |
|----------------|:---------------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| pidigits       | 150 ms                                                          | 147 ms: 1.02x faster                                                          |
| float          | 49.7 ms                                                         | 52.0 ms: 1.04x slower                                                         |
| nbody          | 67.6 ms                                                         | 72.2 ms: 1.07x slower                                                         |
| Geometric mean | (ref)                                                           | 1.03x slower                                                                  |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240605-pythonperf1-amd64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240410-pythonperf1-amd64-faster%2dcpython-call_cmethod-3.13.0a5+-e985127 |
|----------------|:---------------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| regex_dna      | 119 ms                                                          | 115 ms: 1.04x faster                                                          |
| regex_effbot   | 1.58 ms                                                         | 1.55 ms: 1.02x faster                                                         |
| regex_compile  | 78.0 ms                                                         | 80.0 ms: 1.03x slower                                                         |
| Geometric mean | (ref)                                                           | 1.00x faster                                                                  |

Benchmark hidden because not significant (1): regex_v8

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240605-pythonperf1-amd64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240410-pythonperf1-amd64-faster%2dcpython-call_cmethod-3.13.0a5+-e985127 |
|----------------------|:---------------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| json_loads           | 14.2 us                                                         | 13.9 us: 1.02x faster                                                         |
| json_dumps           | 5.61 ms                                                         | 5.72 ms: 1.02x slower                                                         |
| xml_etree_generate   | 53.2 ms                                                         | 54.5 ms: 1.02x slower                                                         |
| xml_etree_parse      | 90.9 ms                                                         | 93.2 ms: 1.02x slower                                                         |
| pickle_dict          | 18.1 us                                                         | 18.6 us: 1.03x slower                                                         |
| pickle_pure_python   | 175 us                                                          | 180 us: 1.03x slower                                                          |
| pickle               | 7.11 us                                                         | 7.36 us: 1.04x slower                                                         |
| xml_etree_process    | 36.4 ms                                                         | 37.8 ms: 1.04x slower                                                         |
| xml_etree_iterparse  | 62.3 ms                                                         | 64.9 ms: 1.04x slower                                                         |
| tomli_loads          | 1.35 sec                                                        | 1.42 sec: 1.05x slower                                                        |
| unpickle_list        | 2.62 us                                                         | 2.79 us: 1.06x slower                                                         |
| unpickle_pure_python | 122 us                                                          | 132 us: 1.08x slower                                                          |
| Geometric mean       | (ref)                                                           | 1.03x slower                                                                  |

Benchmark hidden because not significant (2): unpickle, pickle_list

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240605-pythonperf1-amd64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240410-pythonperf1-amd64-faster%2dcpython-call_cmethod-3.13.0a5+-e985127 |
|------------------------|:---------------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| python_startup         | 20.3 ms                                                         | 19.9 ms: 1.02x faster                                                         |
| python_startup_no_site | 16.2 ms                                                         | 17.8 ms: 1.10x slower                                                         |
| Geometric mean         | (ref)                                                           | 1.04x slower                                                                  |

Benchmarks with tag 'template':
===============================

| Benchmark      | bm-20240605-pythonperf1-amd64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240410-pythonperf1-amd64-faster%2dcpython-call_cmethod-3.13.0a5+-e985127 |
|----------------|:---------------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| genshi_xml     | 31.6 ms                                                         | 35.5 ms: 1.12x slower                                                         |
| genshi_text    | 14.4 ms                                                         | 16.2 ms: 1.13x slower                                                         |
| Geometric mean | (ref)                                                           | 1.08x slower                                                                  |

Benchmark hidden because not significant (1): mako

All benchmarks:
===============

| Benchmark                | bm-20240605-pythonperf1-amd64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240410-pythonperf1-amd64-faster%2dcpython-call_cmethod-3.13.0a5+-e985127 |
|--------------------------|:---------------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| typing_runtime_protocols | 101 us                                                          | 75.2 us: 1.34x faster                                                         |
| pylint                   | 205 ms                                                          | 187 ms: 1.10x faster                                                          |
| json                     | 3.19 ms                                                         | 2.95 ms: 1.08x faster                                                         |
| regex_dna                | 119 ms                                                          | 115 ms: 1.04x faster                                                          |
| regex_effbot             | 1.58 ms                                                         | 1.55 ms: 1.02x faster                                                         |
| python_startup           | 20.3 ms                                                         | 19.9 ms: 1.02x faster                                                         |
| json_loads               | 14.2 us                                                         | 13.9 us: 1.02x faster                                                         |
| pidigits                 | 150 ms                                                          | 147 ms: 1.02x faster                                                          |
| raytrace                 | 162 ms                                                          | 159 ms: 1.02x faster                                                          |
| bench_mp_pool            | 64.8 ms                                                         | 63.8 ms: 1.02x faster                                                         |
| gc_traversal             | 1.55 ms                                                         | 1.54 ms: 1.01x faster                                                         |
| pathlib                  | 75.9 ms                                                         | 75.3 ms: 1.01x faster                                                         |
| thrift                   | 8.11 ms                                                         | 8.07 ms: 1.00x faster                                                         |
| sqlite_synth             | 1.60 us                                                         | 1.60 us: 1.00x slower                                                         |
| chameleon                | 4.80 ms                                                         | 4.84 ms: 1.01x slower                                                         |
| mypy2                    | 418 ms                                                          | 421 ms: 1.01x slower                                                          |
| crypto_pyaes             | 45.5 ms                                                         | 46.1 ms: 1.01x slower                                                         |
| sympy_sum                | 84.4 ms                                                         | 85.6 ms: 1.01x slower                                                         |
| scimark_lu               | 56.6 ms                                                         | 57.7 ms: 1.02x slower                                                         |
| spectral_norm            | 63.7 ms                                                         | 65.0 ms: 1.02x slower                                                         |
| async_tree_io_tg         | 605 ms                                                          | 617 ms: 1.02x slower                                                          |
| json_dumps               | 5.61 ms                                                         | 5.72 ms: 1.02x slower                                                         |
| chaos                    | 38.4 ms                                                         | 39.1 ms: 1.02x slower                                                         |
| async_tree_none          | 218 ms                                                          | 223 ms: 1.02x slower                                                          |
| html5lib                 | 35.0 ms                                                         | 35.8 ms: 1.02x slower                                                         |
| coroutines               | 12.8 ms                                                         | 13.0 ms: 1.02x slower                                                         |
| xml_etree_generate       | 53.2 ms                                                         | 54.5 ms: 1.02x slower                                                         |
| xml_etree_parse          | 90.9 ms                                                         | 93.2 ms: 1.02x slower                                                         |
| pickle_dict              | 18.1 us                                                         | 18.6 us: 1.03x slower                                                         |
| pickle_pure_python       | 175 us                                                          | 180 us: 1.03x slower                                                          |
| sympy_expand             | 271 ms                                                          | 278 ms: 1.03x slower                                                          |
| regex_compile            | 78.0 ms                                                         | 80.0 ms: 1.03x slower                                                         |
| deepcopy                 | 220 us                                                          | 225 us: 1.03x slower                                                          |
| 2to3                     | 207 ms                                                          | 212 ms: 1.03x slower                                                          |
| deepcopy_reduce          | 1.99 us                                                         | 2.05 us: 1.03x slower                                                         |
| sympy_str                | 159 ms                                                          | 164 ms: 1.03x slower                                                          |
| pprint_pformat           | 966 ms                                                          | 997 ms: 1.03x slower                                                          |
| hexiom                   | 3.72 ms                                                         | 3.85 ms: 1.03x slower                                                         |
| sqlglot_transpile        | 955 us                                                          | 987 us: 1.03x slower                                                          |
| bench_thread_pool        | 768 us                                                          | 794 us: 1.03x slower                                                          |
| sqlglot_parse            | 748 us                                                          | 774 us: 1.03x slower                                                          |
| pickle                   | 7.11 us                                                         | 7.36 us: 1.04x slower                                                         |
| async_generators         | 223 ms                                                          | 231 ms: 1.04x slower                                                          |
| pyflate                  | 279 ms                                                          | 289 ms: 1.04x slower                                                          |
| fannkuch                 | 243 ms                                                          | 252 ms: 1.04x slower                                                          |
| xml_etree_process        | 36.4 ms                                                         | 37.8 ms: 1.04x slower                                                         |
| pprint_safe_repr         | 474 ms                                                          | 493 ms: 1.04x slower                                                          |
| logging_format           | 6.22 us                                                         | 6.47 us: 1.04x slower                                                         |
| xml_etree_iterparse      | 62.3 ms                                                         | 64.9 ms: 1.04x slower                                                         |
| sympy_integrate          | 12.2 ms                                                         | 12.8 ms: 1.04x slower                                                         |
| scimark_sor              | 75.3 ms                                                         | 78.7 ms: 1.04x slower                                                         |
| go                       | 82.1 ms                                                         | 85.7 ms: 1.04x slower                                                         |
| float                    | 49.7 ms                                                         | 52.0 ms: 1.04x slower                                                         |
| deltablue                | 1.88 ms                                                         | 1.97 ms: 1.05x slower                                                         |
| scimark_sparse_mat_mult  | 2.50 ms                                                         | 2.62 ms: 1.05x slower                                                         |
| scimark_monte_carlo      | 39.1 ms                                                         | 41.0 ms: 1.05x slower                                                         |
| logging_simple           | 5.78 us                                                         | 6.06 us: 1.05x slower                                                         |
| meteor_contest           | 69.9 ms                                                         | 73.5 ms: 1.05x slower                                                         |
| tomli_loads              | 1.35 sec                                                        | 1.42 sec: 1.05x slower                                                        |
| richards_super           | 30.2 ms                                                         | 31.9 ms: 1.06x slower                                                         |
| dulwich_log              | 38.0 ms                                                         | 40.3 ms: 1.06x slower                                                         |
| sqlglot_optimize         | 32.7 ms                                                         | 34.8 ms: 1.06x slower                                                         |
| unpickle_list            | 2.62 us                                                         | 2.79 us: 1.06x slower                                                         |
| sqlglot_normalize        | 173 ms                                                          | 184 ms: 1.07x slower                                                          |
| nbody                    | 67.6 ms                                                         | 72.2 ms: 1.07x slower                                                         |
| logging_silent           | 52.9 ns                                                         | 56.8 ns: 1.07x slower                                                         |
| telco                    | 4.67 ms                                                         | 5.02 ms: 1.08x slower                                                         |
| comprehensions           | 10.4 us                                                         | 11.2 us: 1.08x slower                                                         |
| async_tree_none_tg       | 202 ms                                                          | 218 ms: 1.08x slower                                                          |
| mdp                      | 1.31 sec                                                        | 1.42 sec: 1.08x slower                                                        |
| unpickle_pure_python     | 122 us                                                          | 132 us: 1.08x slower                                                          |
| scimark_fft              | 171 ms                                                          | 186 ms: 1.09x slower                                                          |
| nqueens                  | 56.7 ms                                                         | 61.7 ms: 1.09x slower                                                         |
| python_startup_no_site   | 16.2 ms                                                         | 17.8 ms: 1.10x slower                                                         |
| coverage                 | 42.1 ms                                                         | 46.4 ms: 1.10x slower                                                         |
| genshi_xml               | 31.6 ms                                                         | 35.5 ms: 1.12x slower                                                         |
| genshi_text              | 14.4 ms                                                         | 16.2 ms: 1.13x slower                                                         |
| generators               | 19.6 ms                                                         | 22.2 ms: 1.13x slower                                                         |
| asyncio_tcp_ssl          | 1.48 sec                                                        | 1.74 sec: 1.17x slower                                                        |
| Geometric mean           | (ref)                                                           | 1.03x slower                                                                  |

Benchmark hidden because not significant (17): pycparser, create_gc_cycles, async_tree_cpu_io_mixed, deepcopy_memo, tornado_http, async_tree_cpu_io_mixed_tg, docutils, unpickle, aiohttp, richards, asyncio_tcp, mako, async_tree_io, pickle_list, async_tree_memoization, regex_v8, async_tree_memoization_tg
Ignored benchmarks (2) of results/bm-20240605-3.13.0b2-3a83b17/bm-20240605-pythonperf1-amd64-python-v3.13.0b2-3.13.0b2-3a83b17.json: django_template, flaskblogging

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.02x
- 95% likely to have a slowdown of 1.02x
- 99% likely to have a slowdown of 1.02x

# Memory
- memory change: unknown