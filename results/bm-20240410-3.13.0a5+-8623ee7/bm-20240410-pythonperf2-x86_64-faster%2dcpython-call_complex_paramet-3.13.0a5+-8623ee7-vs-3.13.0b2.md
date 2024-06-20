# Results vs. 3.13.0b2

- fork: faster-cpython
- ref: call_complex_paramet
- machine: linux-x86_64
- commit hash: 8623ee7
- commit date: 2024-04-10
- overall geometric mean: 1.00x faster
- HPT reliability: 97.53%
- HPT 99th percentile: 1.00x slower
- Memory change: 0.98x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240605-pythonperf2-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240410-pythonperf2-x86_64-faster%2dcpython-call_complex_paramet-3.13.0a5+-8623ee7 |
|----------------|:----------------------------------------------------------------:|:--------------------------------------------------------------------------------------:|
| chameleon      | 7.40 ms                                                          | 7.12 ms: 1.04x faster                                                                  |
| docutils       | 2.98 sec                                                         | 2.99 sec: 1.00x slower                                                                 |
| Geometric mean | (ref)                                                            | 1.01x faster                                                                           |

Benchmark hidden because not significant (3): 2to3, html5lib, tornado_http

Benchmarks with tag 'asyncio':
==============================

| Benchmark      | bm-20240605-pythonperf2-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240410-pythonperf2-x86_64-faster%2dcpython-call_complex_paramet-3.13.0a5+-8623ee7 |
|----------------|:----------------------------------------------------------------:|:--------------------------------------------------------------------------------------:|
| async_tree_io  | 873 ms                                                           | 905 ms: 1.04x slower                                                                   |
| Geometric mean | (ref)                                                            | 1.00x slower                                                                           |

Benchmark hidden because not significant (7): async_tree_io_tg, async_tree_memoization_tg, async_tree_none_tg, async_tree_cpu_io_mixed_tg, async_tree_memoization, async_tree_cpu_io_mixed, async_tree_none

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240605-pythonperf2-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240410-pythonperf2-x86_64-faster%2dcpython-call_complex_paramet-3.13.0a5+-8623ee7 |
|----------------|:----------------------------------------------------------------:|:--------------------------------------------------------------------------------------:|
| float          | 80.2 ms                                                          | 77.2 ms: 1.04x faster                                                                  |
| nbody          | 87.8 ms                                                          | 90.0 ms: 1.02x slower                                                                  |
| pidigits       | 254 ms                                                           | 262 ms: 1.03x slower                                                                   |
| Geometric mean | (ref)                                                            | 1.01x slower                                                                           |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240605-pythonperf2-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240410-pythonperf2-x86_64-faster%2dcpython-call_complex_paramet-3.13.0a5+-8623ee7 |
|----------------|:----------------------------------------------------------------:|:--------------------------------------------------------------------------------------:|
| regex_compile  | 144 ms                                                           | 142 ms: 1.02x faster                                                                   |
| regex_dna      | 249 ms                                                           | 252 ms: 1.01x slower                                                                   |
| regex_effbot   | 3.40 ms                                                          | 3.56 ms: 1.05x slower                                                                  |
| Geometric mean | (ref)                                                            | 1.01x slower                                                                           |

Benchmark hidden because not significant (1): regex_v8

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240605-pythonperf2-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240410-pythonperf2-x86_64-faster%2dcpython-call_complex_paramet-3.13.0a5+-8623ee7 |
|----------------------|:----------------------------------------------------------------:|:--------------------------------------------------------------------------------------:|
| tomli_loads          | 2.40 sec                                                         | 2.19 sec: 1.10x faster                                                                 |
| unpickle             | 15.7 us                                                          | 14.9 us: 1.05x faster                                                                  |
| json_dumps           | 10.8 ms                                                          | 10.5 ms: 1.02x faster                                                                  |
| unpickle_list        | 4.70 us                                                          | 4.60 us: 1.02x faster                                                                  |
| xml_etree_generate   | 85.7 ms                                                          | 84.5 ms: 1.01x faster                                                                  |
| xml_etree_process    | 59.7 ms                                                          | 58.9 ms: 1.01x faster                                                                  |
| unpickle_pure_python | 224 us                                                           | 225 us: 1.00x slower                                                                   |
| xml_etree_parse      | 144 ms                                                           | 146 ms: 1.02x slower                                                                   |
| pickle_pure_python   | 307 us                                                           | 315 us: 1.02x slower                                                                   |
| pickle_dict          | 32.8 us                                                          | 33.6 us: 1.02x slower                                                                  |
| xml_etree_iterparse  | 103 ms                                                           | 105 ms: 1.02x slower                                                                   |
| json_loads           | 25.0 us                                                          | 25.9 us: 1.03x slower                                                                  |
| Geometric mean       | (ref)                                                            | 1.01x faster                                                                           |

Benchmark hidden because not significant (2): pickle_list, pickle

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240605-pythonperf2-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240410-pythonperf2-x86_64-faster%2dcpython-call_complex_paramet-3.13.0a5+-8623ee7 |
|------------------------|:----------------------------------------------------------------:|:--------------------------------------------------------------------------------------:|
| python_startup         | 13.2 ms                                                          | 12.9 ms: 1.03x faster                                                                  |
| python_startup_no_site | 8.85 ms                                                          | 11.1 ms: 1.25x slower                                                                  |
| Geometric mean         | (ref)                                                            | 1.11x slower                                                                           |

Benchmarks with tag 'template':
===============================

| Benchmark      | bm-20240605-pythonperf2-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240410-pythonperf2-x86_64-faster%2dcpython-call_complex_paramet-3.13.0a5+-8623ee7 |
|----------------|:----------------------------------------------------------------:|:--------------------------------------------------------------------------------------:|
| genshi_xml     | 58.1 ms                                                          | 54.3 ms: 1.07x faster                                                                  |
| genshi_text    | 25.9 ms                                                          | 25.1 ms: 1.03x faster                                                                  |
| mako           | 10.4 ms                                                          | 10.2 ms: 1.01x faster                                                                  |
| Geometric mean | (ref)                                                            | 1.04x faster                                                                           |

All benchmarks:
===============

| Benchmark                | bm-20240605-pythonperf2-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240410-pythonperf2-x86_64-faster%2dcpython-call_complex_paramet-3.13.0a5+-8623ee7 |
|--------------------------|:----------------------------------------------------------------:|:--------------------------------------------------------------------------------------:|
| typing_runtime_protocols | 171 us                                                           | 114 us: 1.50x faster                                                                   |
| tomli_loads              | 2.40 sec                                                         | 2.19 sec: 1.10x faster                                                                 |
| pylint                   | 339 ms                                                           | 317 ms: 1.07x faster                                                                   |
| create_gc_cycles         | 2.00 ms                                                          | 1.87 ms: 1.07x faster                                                                  |
| genshi_xml               | 58.1 ms                                                          | 54.3 ms: 1.07x faster                                                                  |
| bench_mp_pool            | 4.91 ms                                                          | 4.61 ms: 1.07x faster                                                                  |
| richards_super           | 61.2 ms                                                          | 58.2 ms: 1.05x faster                                                                  |
| unpickle                 | 15.7 us                                                          | 14.9 us: 1.05x faster                                                                  |
| scimark_fft              | 312 ms                                                           | 297 ms: 1.05x faster                                                                   |
| float                    | 80.2 ms                                                          | 77.2 ms: 1.04x faster                                                                  |
| chameleon                | 7.40 ms                                                          | 7.12 ms: 1.04x faster                                                                  |
| telco                    | 8.40 ms                                                          | 8.11 ms: 1.04x faster                                                                  |
| genshi_text              | 25.9 ms                                                          | 25.1 ms: 1.03x faster                                                                  |
| pprint_safe_repr         | 818 ms                                                           | 792 ms: 1.03x faster                                                                   |
| python_startup           | 13.2 ms                                                          | 12.9 ms: 1.03x faster                                                                  |
| pprint_pformat           | 1.66 sec                                                         | 1.62 sec: 1.03x faster                                                                 |
| spectral_norm            | 97.3 ms                                                          | 95.0 ms: 1.02x faster                                                                  |
| crypto_pyaes             | 73.6 ms                                                          | 71.8 ms: 1.02x faster                                                                  |
| scimark_lu               | 97.5 ms                                                          | 95.2 ms: 1.02x faster                                                                  |
| richards                 | 53.4 ms                                                          | 52.2 ms: 1.02x faster                                                                  |
| comprehensions           | 17.0 us                                                          | 16.6 us: 1.02x faster                                                                  |
| sqlglot_normalize        | 120 ms                                                           | 118 ms: 1.02x faster                                                                   |
| bench_thread_pool        | 908 us                                                           | 888 us: 1.02x faster                                                                   |
| json_dumps               | 10.8 ms                                                          | 10.5 ms: 1.02x faster                                                                  |
| unpickle_list            | 4.70 us                                                          | 4.60 us: 1.02x faster                                                                  |
| sqlite_synth             | 2.80 us                                                          | 2.74 us: 1.02x faster                                                                  |
| regex_compile            | 144 ms                                                           | 142 ms: 1.02x faster                                                                   |
| sqlglot_optimize         | 59.5 ms                                                          | 58.6 ms: 1.02x faster                                                                  |
| mako                     | 10.4 ms                                                          | 10.2 ms: 1.01x faster                                                                  |
| asyncio_tcp              | 378 ms                                                           | 372 ms: 1.01x faster                                                                   |
| xml_etree_generate       | 85.7 ms                                                          | 84.5 ms: 1.01x faster                                                                  |
| xml_etree_process        | 59.7 ms                                                          | 58.9 ms: 1.01x faster                                                                  |
| logging_silent           | 96.3 ns                                                          | 95.3 ns: 1.01x faster                                                                  |
| scimark_sparse_mat_mult  | 4.28 ms                                                          | 4.24 ms: 1.01x faster                                                                  |
| raytrace                 | 260 ms                                                           | 258 ms: 1.01x faster                                                                   |
| sympy_expand             | 501 ms                                                           | 499 ms: 1.00x faster                                                                   |
| sympy_str                | 295 ms                                                           | 296 ms: 1.00x slower                                                                   |
| docutils                 | 2.98 sec                                                         | 2.99 sec: 1.00x slower                                                                 |
| async_generators         | 363 ms                                                           | 364 ms: 1.00x slower                                                                   |
| unpickle_pure_python     | 224 us                                                           | 225 us: 1.00x slower                                                                   |
| chaos                    | 59.6 ms                                                          | 59.9 ms: 1.00x slower                                                                  |
| meteor_contest           | 128 ms                                                           | 129 ms: 1.01x slower                                                                   |
| regex_dna                | 249 ms                                                           | 252 ms: 1.01x slower                                                                   |
| sqlglot_transpile        | 1.76 ms                                                          | 1.78 ms: 1.01x slower                                                                  |
| sympy_integrate          | 23.2 ms                                                          | 23.4 ms: 1.01x slower                                                                  |
| dulwich_log              | 67.3 ms                                                          | 68.0 ms: 1.01x slower                                                                  |
| deepcopy_memo            | 37.3 us                                                          | 37.8 us: 1.01x slower                                                                  |
| hexiom                   | 6.35 ms                                                          | 6.45 ms: 1.02x slower                                                                  |
| xml_etree_parse          | 144 ms                                                           | 146 ms: 1.02x slower                                                                   |
| nqueens                  | 88.4 ms                                                          | 90.1 ms: 1.02x slower                                                                  |
| coroutines               | 22.0 ms                                                          | 22.4 ms: 1.02x slower                                                                  |
| logging_format           | 7.11 us                                                          | 7.27 us: 1.02x slower                                                                  |
| coverage                 | 83.5 ms                                                          | 85.3 ms: 1.02x slower                                                                  |
| deltablue                | 3.37 ms                                                          | 3.45 ms: 1.02x slower                                                                  |
| pickle_pure_python       | 307 us                                                           | 315 us: 1.02x slower                                                                   |
| pickle_dict              | 32.8 us                                                          | 33.6 us: 1.02x slower                                                                  |
| nbody                    | 87.8 ms                                                          | 90.0 ms: 1.02x slower                                                                  |
| xml_etree_iterparse      | 103 ms                                                           | 105 ms: 1.02x slower                                                                   |
| deepcopy                 | 377 us                                                           | 387 us: 1.03x slower                                                                   |
| deepcopy_reduce          | 3.39 us                                                          | 3.48 us: 1.03x slower                                                                  |
| logging_simple           | 6.40 us                                                          | 6.59 us: 1.03x slower                                                                  |
| json_loads               | 25.0 us                                                          | 25.9 us: 1.03x slower                                                                  |
| go                       | 165 ms                                                           | 170 ms: 1.03x slower                                                                   |
| json                     | 5.35 ms                                                          | 5.53 ms: 1.03x slower                                                                  |
| mdp                      | 2.46 sec                                                         | 2.54 sec: 1.03x slower                                                                 |
| pidigits                 | 254 ms                                                           | 262 ms: 1.03x slower                                                                   |
| async_tree_io            | 873 ms                                                           | 905 ms: 1.04x slower                                                                   |
| pycparser                | 1.22 sec                                                         | 1.27 sec: 1.04x slower                                                                 |
| regex_effbot             | 3.40 ms                                                          | 3.56 ms: 1.05x slower                                                                  |
| scimark_monte_carlo      | 65.5 ms                                                          | 70.1 ms: 1.07x slower                                                                  |
| pyflate                  | 482 ms                                                           | 523 ms: 1.09x slower                                                                   |
| fannkuch                 | 353 ms                                                           | 392 ms: 1.11x slower                                                                   |
| pathlib                  | 17.1 ms                                                          | 19.4 ms: 1.14x slower                                                                  |
| scimark_sor              | 119 ms                                                           | 141 ms: 1.19x slower                                                                   |
| python_startup_no_site   | 8.85 ms                                                          | 11.1 ms: 1.25x slower                                                                  |
| Geometric mean           | (ref)                                                            | 1.00x faster                                                                           |

Benchmark hidden because not significant (24): async_tree_io_tg, pickle_list, gunicorn, async_tree_memoization_tg, async_tree_none_tg, pickle, asyncio_tcp_ssl, gc_traversal, regex_v8, html5lib, thrift, asyncio_websockets, 2to3, async_tree_cpu_io_mixed_tg, aiohttp, sympy_sum, generators, tornado_http, sqlglot_parse, async_tree_memoization, async_tree_cpu_io_mixed, async_tree_none, dask, mypy2
Ignored benchmarks (3) of results/bm-20240605-3.13.0b2-3a83b17/bm-20240605-pythonperf2-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17.json: bpe_tokeniser, django_template, flaskblogging

# HPT report

- Reliability score: 97.53% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 0.98x