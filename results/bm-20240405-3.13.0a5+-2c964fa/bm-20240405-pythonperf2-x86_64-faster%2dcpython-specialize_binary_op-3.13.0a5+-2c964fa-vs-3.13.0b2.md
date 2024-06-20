# Results vs. 3.13.0b2

- fork: faster-cpython
- ref: specialize_binary_op
- machine: linux-x86_64
- commit hash: 2c964fa
- commit date: 2024-04-05
- overall geometric mean: 1.01x faster
- HPT reliability: 52.50%
- HPT 99th percentile: 1.00x slower
- Memory change: 0.98x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240605-pythonperf2-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240405-pythonperf2-x86_64-faster%2dcpython-specialize_binary_op-3.13.0a5+-2c964fa |
|----------------|:----------------------------------------------------------------:|:--------------------------------------------------------------------------------------:|
| 2to3           | 291 ms                                                           | 288 ms: 1.01x faster                                                                   |
| chameleon      | 7.40 ms                                                          | 7.47 ms: 1.01x slower                                                                  |
| html5lib       | 74.7 ms                                                          | 73.9 ms: 1.01x faster                                                                  |
| Geometric mean | (ref)                                                            | 1.00x faster                                                                           |

Benchmark hidden because not significant (2): docutils, tornado_http

Benchmarks with tag 'asyncio':
==============================

| Benchmark      | bm-20240605-pythonperf2-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240405-pythonperf2-x86_64-faster%2dcpython-specialize_binary_op-3.13.0a5+-2c964fa |
|----------------|:----------------------------------------------------------------:|:--------------------------------------------------------------------------------------:|
| async_tree_io  | 873 ms                                                           | 907 ms: 1.04x slower                                                                   |
| Geometric mean | (ref)                                                            | 1.00x slower                                                                           |

Benchmark hidden because not significant (7): async_tree_none_tg, async_tree_io_tg, async_tree_memoization_tg, async_tree_memoization, async_tree_cpu_io_mixed_tg, async_tree_none, async_tree_cpu_io_mixed

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240605-pythonperf2-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240405-pythonperf2-x86_64-faster%2dcpython-specialize_binary_op-3.13.0a5+-2c964fa |
|----------------|:----------------------------------------------------------------:|:--------------------------------------------------------------------------------------:|
| float          | 80.2 ms                                                          | 76.4 ms: 1.05x faster                                                                  |
| pidigits       | 254 ms                                                           | 262 ms: 1.03x slower                                                                   |
| nbody          | 87.8 ms                                                          | 91.4 ms: 1.04x slower                                                                  |
| Geometric mean | (ref)                                                            | 1.01x slower                                                                           |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240605-pythonperf2-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240405-pythonperf2-x86_64-faster%2dcpython-specialize_binary_op-3.13.0a5+-2c964fa |
|----------------|:----------------------------------------------------------------:|:--------------------------------------------------------------------------------------:|
| regex_dna      | 249 ms                                                           | 240 ms: 1.04x faster                                                                   |
| regex_v8       | 26.0 ms                                                          | 25.4 ms: 1.02x faster                                                                  |
| regex_compile  | 144 ms                                                           | 141 ms: 1.02x faster                                                                   |
| regex_effbot   | 3.40 ms                                                          | 3.48 ms: 1.02x slower                                                                  |
| Geometric mean | (ref)                                                            | 1.01x faster                                                                           |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240605-pythonperf2-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240405-pythonperf2-x86_64-faster%2dcpython-specialize_binary_op-3.13.0a5+-2c964fa |
|----------------------|:----------------------------------------------------------------:|:--------------------------------------------------------------------------------------:|
| tomli_loads          | 2.40 sec                                                         | 2.20 sec: 1.09x faster                                                                 |
| pickle_dict          | 32.8 us                                                          | 30.4 us: 1.08x faster                                                                  |
| pickle               | 10.6 us                                                          | 10.2 us: 1.04x faster                                                                  |
| xml_etree_generate   | 85.7 ms                                                          | 82.6 ms: 1.04x faster                                                                  |
| pickle_list          | 4.44 us                                                          | 4.29 us: 1.04x faster                                                                  |
| xml_etree_process    | 59.7 ms                                                          | 57.6 ms: 1.04x faster                                                                  |
| unpickle             | 15.7 us                                                          | 15.2 us: 1.03x faster                                                                  |
| unpickle_list        | 4.70 us                                                          | 4.57 us: 1.03x faster                                                                  |
| json_dumps           | 10.8 ms                                                          | 10.6 ms: 1.02x faster                                                                  |
| unpickle_pure_python | 224 us                                                           | 221 us: 1.01x faster                                                                   |
| xml_etree_iterparse  | 103 ms                                                           | 104 ms: 1.02x slower                                                                   |
| json_loads           | 25.0 us                                                          | 25.5 us: 1.02x slower                                                                  |
| xml_etree_parse      | 144 ms                                                           | 148 ms: 1.03x slower                                                                   |
| Geometric mean       | (ref)                                                            | 1.02x faster                                                                           |

Benchmark hidden because not significant (1): pickle_pure_python

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240605-pythonperf2-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240405-pythonperf2-x86_64-faster%2dcpython-specialize_binary_op-3.13.0a5+-2c964fa |
|------------------------|:----------------------------------------------------------------:|:--------------------------------------------------------------------------------------:|
| python_startup         | 13.2 ms                                                          | 12.8 ms: 1.03x faster                                                                  |
| python_startup_no_site | 8.85 ms                                                          | 11.0 ms: 1.25x slower                                                                  |
| Geometric mean         | (ref)                                                            | 1.10x slower                                                                           |

Benchmarks with tag 'template':
===============================

| Benchmark      | bm-20240605-pythonperf2-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240405-pythonperf2-x86_64-faster%2dcpython-specialize_binary_op-3.13.0a5+-2c964fa |
|----------------|:----------------------------------------------------------------:|:--------------------------------------------------------------------------------------:|
| genshi_xml     | 58.1 ms                                                          | 53.5 ms: 1.08x faster                                                                  |
| genshi_text    | 25.9 ms                                                          | 24.7 ms: 1.05x faster                                                                  |
| mako           | 10.4 ms                                                          | 10.3 ms: 1.01x faster                                                                  |
| Geometric mean | (ref)                                                            | 1.05x faster                                                                           |

All benchmarks:
===============

| Benchmark                | bm-20240605-pythonperf2-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240405-pythonperf2-x86_64-faster%2dcpython-specialize_binary_op-3.13.0a5+-2c964fa |
|--------------------------|:----------------------------------------------------------------:|:--------------------------------------------------------------------------------------:|
| typing_runtime_protocols | 171 us                                                           | 116 us: 1.48x faster                                                                   |
| spectral_norm            | 97.3 ms                                                          | 88.4 ms: 1.10x faster                                                                  |
| tomli_loads              | 2.40 sec                                                         | 2.20 sec: 1.09x faster                                                                 |
| genshi_xml               | 58.1 ms                                                          | 53.5 ms: 1.08x faster                                                                  |
| pickle_dict              | 32.8 us                                                          | 30.4 us: 1.08x faster                                                                  |
| bench_mp_pool            | 4.91 ms                                                          | 4.55 ms: 1.08x faster                                                                  |
| pylint                   | 339 ms                                                           | 318 ms: 1.07x faster                                                                   |
| telco                    | 8.40 ms                                                          | 7.91 ms: 1.06x faster                                                                  |
| richards_super           | 61.2 ms                                                          | 58.3 ms: 1.05x faster                                                                  |
| float                    | 80.2 ms                                                          | 76.4 ms: 1.05x faster                                                                  |
| genshi_text              | 25.9 ms                                                          | 24.7 ms: 1.05x faster                                                                  |
| create_gc_cycles         | 2.00 ms                                                          | 1.92 ms: 1.04x faster                                                                  |
| pprint_safe_repr         | 818 ms                                                           | 785 ms: 1.04x faster                                                                   |
| regex_dna                | 249 ms                                                           | 240 ms: 1.04x faster                                                                   |
| pprint_pformat           | 1.66 sec                                                         | 1.60 sec: 1.04x faster                                                                 |
| pickle                   | 10.6 us                                                          | 10.2 us: 1.04x faster                                                                  |
| xml_etree_generate       | 85.7 ms                                                          | 82.6 ms: 1.04x faster                                                                  |
| pickle_list              | 4.44 us                                                          | 4.29 us: 1.04x faster                                                                  |
| sqlglot_normalize        | 120 ms                                                           | 116 ms: 1.04x faster                                                                   |
| xml_etree_process        | 59.7 ms                                                          | 57.6 ms: 1.04x faster                                                                  |
| richards                 | 53.4 ms                                                          | 51.7 ms: 1.03x faster                                                                  |
| unpickle                 | 15.7 us                                                          | 15.2 us: 1.03x faster                                                                  |
| python_startup           | 13.2 ms                                                          | 12.8 ms: 1.03x faster                                                                  |
| unpickle_list            | 4.70 us                                                          | 4.57 us: 1.03x faster                                                                  |
| comprehensions           | 17.0 us                                                          | 16.5 us: 1.03x faster                                                                  |
| bench_thread_pool        | 908 us                                                           | 886 us: 1.02x faster                                                                   |
| sqlglot_optimize         | 59.5 ms                                                          | 58.1 ms: 1.02x faster                                                                  |
| logging_silent           | 96.3 ns                                                          | 94.0 ns: 1.02x faster                                                                  |
| asyncio_tcp              | 378 ms                                                           | 369 ms: 1.02x faster                                                                   |
| regex_v8                 | 26.0 ms                                                          | 25.4 ms: 1.02x faster                                                                  |
| regex_compile            | 144 ms                                                           | 141 ms: 1.02x faster                                                                   |
| sqlite_synth             | 2.80 us                                                          | 2.74 us: 1.02x faster                                                                  |
| gc_traversal             | 4.69 ms                                                          | 4.60 ms: 1.02x faster                                                                  |
| generators               | 33.5 ms                                                          | 32.9 ms: 1.02x faster                                                                  |
| json_dumps               | 10.8 ms                                                          | 10.6 ms: 1.02x faster                                                                  |
| crypto_pyaes             | 73.6 ms                                                          | 72.4 ms: 1.02x faster                                                                  |
| thrift                   | 880 us                                                           | 867 us: 1.01x faster                                                                   |
| unpickle_pure_python     | 224 us                                                           | 221 us: 1.01x faster                                                                   |
| sympy_expand             | 501 ms                                                           | 495 ms: 1.01x faster                                                                   |
| async_generators         | 363 ms                                                           | 359 ms: 1.01x faster                                                                   |
| mako                     | 10.4 ms                                                          | 10.3 ms: 1.01x faster                                                                  |
| 2to3                     | 291 ms                                                           | 288 ms: 1.01x faster                                                                   |
| html5lib                 | 74.7 ms                                                          | 73.9 ms: 1.01x faster                                                                  |
| sympy_sum                | 155 ms                                                           | 153 ms: 1.01x faster                                                                   |
| raytrace                 | 260 ms                                                           | 258 ms: 1.01x faster                                                                   |
| meteor_contest           | 128 ms                                                           | 127 ms: 1.01x faster                                                                   |
| asyncio_tcp_ssl          | 1.58 sec                                                         | 1.58 sec: 1.00x faster                                                                 |
| sqlglot_transpile        | 1.76 ms                                                          | 1.77 ms: 1.00x slower                                                                  |
| sympy_integrate          | 23.2 ms                                                          | 23.3 ms: 1.01x slower                                                                  |
| chameleon                | 7.40 ms                                                          | 7.47 ms: 1.01x slower                                                                  |
| dulwich_log              | 67.3 ms                                                          | 68.1 ms: 1.01x slower                                                                  |
| sqlglot_parse            | 1.39 ms                                                          | 1.41 ms: 1.01x slower                                                                  |
| scimark_lu               | 97.5 ms                                                          | 98.7 ms: 1.01x slower                                                                  |
| nqueens                  | 88.4 ms                                                          | 89.5 ms: 1.01x slower                                                                  |
| deepcopy_reduce          | 3.39 us                                                          | 3.43 us: 1.01x slower                                                                  |
| deltablue                | 3.37 ms                                                          | 3.42 ms: 1.01x slower                                                                  |
| logging_simple           | 6.40 us                                                          | 6.49 us: 1.01x slower                                                                  |
| scimark_sparse_mat_mult  | 4.28 ms                                                          | 4.35 ms: 1.01x slower                                                                  |
| chaos                    | 59.6 ms                                                          | 60.7 ms: 1.02x slower                                                                  |
| logging_format           | 7.11 us                                                          | 7.24 us: 1.02x slower                                                                  |
| xml_etree_iterparse      | 103 ms                                                           | 104 ms: 1.02x slower                                                                   |
| json_loads               | 25.0 us                                                          | 25.5 us: 1.02x slower                                                                  |
| mdp                      | 2.46 sec                                                         | 2.51 sec: 1.02x slower                                                                 |
| json                     | 5.35 ms                                                          | 5.48 ms: 1.02x slower                                                                  |
| hexiom                   | 6.35 ms                                                          | 6.50 ms: 1.02x slower                                                                  |
| regex_effbot             | 3.40 ms                                                          | 3.48 ms: 1.02x slower                                                                  |
| scimark_fft              | 312 ms                                                           | 320 ms: 1.03x slower                                                                   |
| xml_etree_parse          | 144 ms                                                           | 148 ms: 1.03x slower                                                                   |
| pidigits                 | 254 ms                                                           | 262 ms: 1.03x slower                                                                   |
| coroutines               | 22.0 ms                                                          | 22.7 ms: 1.03x slower                                                                  |
| pycparser                | 1.22 sec                                                         | 1.26 sec: 1.03x slower                                                                 |
| async_tree_io            | 873 ms                                                           | 907 ms: 1.04x slower                                                                   |
| nbody                    | 87.8 ms                                                          | 91.4 ms: 1.04x slower                                                                  |
| scimark_monte_carlo      | 65.5 ms                                                          | 68.2 ms: 1.04x slower                                                                  |
| go                       | 165 ms                                                           | 173 ms: 1.05x slower                                                                   |
| pyflate                  | 482 ms                                                           | 507 ms: 1.05x slower                                                                   |
| coverage                 | 83.5 ms                                                          | 89.1 ms: 1.07x slower                                                                  |
| fannkuch                 | 353 ms                                                           | 381 ms: 1.08x slower                                                                   |
| pathlib                  | 17.1 ms                                                          | 19.1 ms: 1.12x slower                                                                  |
| scimark_sor              | 119 ms                                                           | 139 ms: 1.17x slower                                                                   |
| python_startup_no_site   | 8.85 ms                                                          | 11.0 ms: 1.25x slower                                                                  |
| Geometric mean           | (ref)                                                            | 1.01x faster                                                                           |

Benchmark hidden because not significant (18): async_tree_none_tg, async_tree_io_tg, async_tree_memoization_tg, asyncio_websockets, dask, deepcopy_memo, pickle_pure_python, sympy_str, docutils, gunicorn, tornado_http, async_tree_memoization, async_tree_cpu_io_mixed_tg, mypy2, async_tree_none, aiohttp, deepcopy, async_tree_cpu_io_mixed
Ignored benchmarks (3) of results/bm-20240605-3.13.0b2-3a83b17/bm-20240605-pythonperf2-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17.json: bpe_tokeniser, django_template, flaskblogging

# HPT report

- Reliability score: 52.50% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 0.98x