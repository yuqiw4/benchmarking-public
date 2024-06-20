# Results vs. 3.13.0b2

- fork: faster-cpython
- ref: interpreter_reentry_
- machine: linux-x86_64
- commit hash: 8069375
- commit date: 2024-04-02
- overall geometric mean: 1.02x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.00x faster
- Memory change: 0.98x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240402-linux-x86_64-faster%2dcpython-interpreter_reentry_-3.13.0a5+-8069375 |
|----------------|:----------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| 2to3           | 274 ms                                                     | 268 ms: 1.02x faster                                                             |
| chameleon      | 7.22 ms                                                    | 6.81 ms: 1.06x faster                                                            |
| docutils       | 2.83 sec                                                   | 2.77 sec: 1.02x faster                                                           |
| html5lib       | 67.2 ms                                                    | 66.7 ms: 1.01x faster                                                            |
| Geometric mean | (ref)                                                      | 1.02x faster                                                                     |

Benchmark hidden because not significant (1): tornado_http

Benchmarks with tag 'asyncio':
==============================

| Benchmark              | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240402-linux-x86_64-faster%2dcpython-interpreter_reentry_-3.13.0a5+-8069375 |
|------------------------|:----------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| async_tree_memoization | 463 ms                                                     | 438 ms: 1.06x faster                                                             |
| async_tree_io          | 939 ms                                                     | 900 ms: 1.04x faster                                                             |
| Geometric mean         | (ref)                                                      | 1.01x faster                                                                     |

Benchmark hidden because not significant (6): async_tree_cpu_io_mixed, async_tree_cpu_io_mixed_tg, async_tree_none_tg, async_tree_io_tg, async_tree_memoization_tg, async_tree_none

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240402-linux-x86_64-faster%2dcpython-interpreter_reentry_-3.13.0a5+-8069375 |
|----------------|:----------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| float          | 78.9 ms                                                    | 76.6 ms: 1.03x faster                                                            |
| pidigits       | 191 ms                                                     | 190 ms: 1.01x faster                                                             |
| nbody          | 88.3 ms                                                    | 87.7 ms: 1.01x faster                                                            |
| Geometric mean | (ref)                                                      | 1.02x faster                                                                     |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240402-linux-x86_64-faster%2dcpython-interpreter_reentry_-3.13.0a5+-8069375 |
|----------------|:----------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| regex_compile  | 137 ms                                                     | 133 ms: 1.03x faster                                                             |
| regex_v8       | 25.1 ms                                                    | 24.7 ms: 1.02x faster                                                            |
| regex_effbot   | 3.67 ms                                                    | 3.65 ms: 1.01x faster                                                            |
| regex_dna      | 221 ms                                                     | 220 ms: 1.01x faster                                                             |
| Geometric mean | (ref)                                                      | 1.01x faster                                                                     |

Benchmarks with tag 'serialize':
================================

| Benchmark           | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240402-linux-x86_64-faster%2dcpython-interpreter_reentry_-3.13.0a5+-8069375 |
|---------------------|:----------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| pickle_list         | 5.11 us                                                    | 4.94 us: 1.03x faster                                                            |
| xml_etree_process   | 61.2 ms                                                    | 59.5 ms: 1.03x faster                                                            |
| pickle_dict         | 34.8 us                                                    | 34.0 us: 1.02x faster                                                            |
| json_loads          | 28.9 us                                                    | 28.4 us: 1.02x faster                                                            |
| json_dumps          | 10.7 ms                                                    | 10.6 ms: 1.02x faster                                                            |
| pickle_pure_python  | 305 us                                                     | 301 us: 1.01x faster                                                             |
| xml_etree_iterparse | 107 ms                                                     | 106 ms: 1.01x faster                                                             |
| xml_etree_generate  | 87.4 ms                                                    | 86.4 ms: 1.01x faster                                                            |
| unpickle_list       | 5.34 us                                                    | 5.31 us: 1.01x faster                                                            |
| pickle              | 11.5 us                                                    | 11.7 us: 1.02x slower                                                            |
| tomli_loads         | 2.12 sec                                                   | 2.22 sec: 1.05x slower                                                           |
| unpickle            | 15.1 us                                                    | 16.2 us: 1.07x slower                                                            |
| Geometric mean      | (ref)                                                      | 1.00x faster                                                                     |

Benchmark hidden because not significant (2): xml_etree_parse, unpickle_pure_python

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240402-linux-x86_64-faster%2dcpython-interpreter_reentry_-3.13.0a5+-8069375 |
|------------------------|:----------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| python_startup         | 10.8 ms                                                    | 10.7 ms: 1.01x faster                                                            |
| python_startup_no_site | 7.11 ms                                                    | 9.03 ms: 1.27x slower                                                            |
| Geometric mean         | (ref)                                                      | 1.12x slower                                                                     |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240402-linux-x86_64-faster%2dcpython-interpreter_reentry_-3.13.0a5+-8069375 |
|-----------------|:----------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| mako            | 11.2 ms                                                    | 10.9 ms: 1.03x faster                                                            |
| django_template | 34.8 ms                                                    | 34.5 ms: 1.01x faster                                                            |
| genshi_xml      | 51.6 ms                                                    | 52.5 ms: 1.02x slower                                                            |
| genshi_text     | 23.7 ms                                                    | 24.3 ms: 1.03x slower                                                            |
| Geometric mean  | (ref)                                                      | 1.00x slower                                                                     |

All benchmarks:
===============

| Benchmark                | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240402-linux-x86_64-faster%2dcpython-interpreter_reentry_-3.13.0a5+-8069375 |
|--------------------------|:----------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| typing_runtime_protocols | 165 us                                                     | 114 us: 1.44x faster                                                             |
| scimark_sparse_mat_mult  | 5.27 ms                                                    | 4.61 ms: 1.14x faster                                                            |
| pylint                   | 317 ms                                                     | 280 ms: 1.13x faster                                                             |
| richards                 | 50.9 ms                                                    | 45.6 ms: 1.12x faster                                                            |
| gc_traversal             | 3.98 ms                                                    | 3.57 ms: 1.11x faster                                                            |
| richards_super           | 57.4 ms                                                    | 51.8 ms: 1.11x faster                                                            |
| scimark_fft              | 392 ms                                                     | 359 ms: 1.09x faster                                                             |
| create_gc_cycles         | 1.82 ms                                                    | 1.67 ms: 1.09x faster                                                            |
| mdp                      | 2.79 sec                                                   | 2.56 sec: 1.09x faster                                                           |
| scimark_lu               | 122 ms                                                     | 113 ms: 1.07x faster                                                             |
| deepcopy_reduce          | 3.35 us                                                    | 3.13 us: 1.07x faster                                                            |
| spectral_norm            | 116 ms                                                     | 109 ms: 1.07x faster                                                             |
| chameleon                | 7.22 ms                                                    | 6.81 ms: 1.06x faster                                                            |
| async_tree_memoization   | 463 ms                                                     | 438 ms: 1.06x faster                                                             |
| deepcopy_memo            | 39.7 us                                                    | 37.7 us: 1.05x faster                                                            |
| scimark_sor              | 127 ms                                                     | 121 ms: 1.05x faster                                                             |
| deepcopy                 | 367 us                                                     | 350 us: 1.05x faster                                                             |
| async_tree_io            | 939 ms                                                     | 900 ms: 1.04x faster                                                             |
| crypto_pyaes             | 77.5 ms                                                    | 74.4 ms: 1.04x faster                                                            |
| logging_silent           | 105 ns                                                     | 101 ns: 1.04x faster                                                             |
| go                       | 145 ms                                                     | 139 ms: 1.04x faster                                                             |
| sqlglot_parse            | 1.32 ms                                                    | 1.27 ms: 1.04x faster                                                            |
| scimark_monte_carlo      | 69.2 ms                                                    | 66.8 ms: 1.04x faster                                                            |
| sqlite_synth             | 2.99 us                                                    | 2.89 us: 1.03x faster                                                            |
| hexiom                   | 6.30 ms                                                    | 6.09 ms: 1.03x faster                                                            |
| pickle_list              | 5.11 us                                                    | 4.94 us: 1.03x faster                                                            |
| pyflate                  | 484 ms                                                     | 469 ms: 1.03x faster                                                             |
| sympy_str                | 282 ms                                                     | 274 ms: 1.03x faster                                                             |
| float                    | 78.9 ms                                                    | 76.6 ms: 1.03x faster                                                            |
| mako                     | 11.2 ms                                                    | 10.9 ms: 1.03x faster                                                            |
| regex_compile            | 137 ms                                                     | 133 ms: 1.03x faster                                                             |
| sqlglot_transpile        | 1.63 ms                                                    | 1.59 ms: 1.03x faster                                                            |
| xml_etree_process        | 61.2 ms                                                    | 59.5 ms: 1.03x faster                                                            |
| coroutines               | 23.2 ms                                                    | 22.6 ms: 1.03x faster                                                            |
| sympy_integrate          | 20.5 ms                                                    | 20.0 ms: 1.03x faster                                                            |
| chaos                    | 61.3 ms                                                    | 59.8 ms: 1.03x faster                                                            |
| deltablue                | 3.25 ms                                                    | 3.17 ms: 1.03x faster                                                            |
| 2to3                     | 274 ms                                                     | 268 ms: 1.02x faster                                                             |
| docutils                 | 2.83 sec                                                   | 2.77 sec: 1.02x faster                                                           |
| pickle_dict              | 34.8 us                                                    | 34.0 us: 1.02x faster                                                            |
| sympy_expand             | 473 ms                                                     | 463 ms: 1.02x faster                                                             |
| raytrace                 | 267 ms                                                     | 261 ms: 1.02x faster                                                             |
| sqlglot_optimize         | 55.5 ms                                                    | 54.5 ms: 1.02x faster                                                            |
| json_loads               | 28.9 us                                                    | 28.4 us: 1.02x faster                                                            |
| sqlglot_normalize        | 110 ms                                                     | 108 ms: 1.02x faster                                                             |
| asyncio_tcp              | 508 ms                                                     | 500 ms: 1.02x faster                                                             |
| json_dumps               | 10.7 ms                                                    | 10.6 ms: 1.02x faster                                                            |
| pprint_pformat           | 1.56 sec                                                   | 1.53 sec: 1.02x faster                                                           |
| pprint_safe_repr         | 758 ms                                                     | 747 ms: 1.02x faster                                                             |
| thrift                   | 823 us                                                     | 810 us: 1.02x faster                                                             |
| regex_v8                 | 25.1 ms                                                    | 24.7 ms: 1.02x faster                                                            |
| fannkuch                 | 402 ms                                                     | 396 ms: 1.02x faster                                                             |
| sympy_sum                | 156 ms                                                     | 153 ms: 1.02x faster                                                             |
| pickle_pure_python       | 305 us                                                     | 301 us: 1.01x faster                                                             |
| meteor_contest           | 110 ms                                                     | 108 ms: 1.01x faster                                                             |
| xml_etree_iterparse      | 107 ms                                                     | 106 ms: 1.01x faster                                                             |
| xml_etree_generate       | 87.4 ms                                                    | 86.4 ms: 1.01x faster                                                            |
| comprehensions           | 16.6 us                                                    | 16.4 us: 1.01x faster                                                            |
| django_template          | 34.8 ms                                                    | 34.5 ms: 1.01x faster                                                            |
| pidigits                 | 191 ms                                                     | 190 ms: 1.01x faster                                                             |
| python_startup           | 10.8 ms                                                    | 10.7 ms: 1.01x faster                                                            |
| nqueens                  | 81.4 ms                                                    | 80.7 ms: 1.01x faster                                                            |
| html5lib                 | 67.2 ms                                                    | 66.7 ms: 1.01x faster                                                            |
| unpickle_list            | 5.34 us                                                    | 5.31 us: 1.01x faster                                                            |
| bench_thread_pool        | 834 us                                                     | 828 us: 1.01x faster                                                             |
| nbody                    | 88.3 ms                                                    | 87.7 ms: 1.01x faster                                                            |
| regex_effbot             | 3.67 ms                                                    | 3.65 ms: 1.01x faster                                                            |
| regex_dna                | 221 ms                                                     | 220 ms: 1.01x faster                                                             |
| dulwich_log              | 67.2 ms                                                    | 66.8 ms: 1.00x faster                                                            |
| asyncio_tcp_ssl          | 1.84 sec                                                   | 1.83 sec: 1.00x faster                                                           |
| generators               | 29.6 ms                                                    | 30.0 ms: 1.01x slower                                                            |
| telco                    | 8.41 ms                                                    | 8.54 ms: 1.01x slower                                                            |
| pycparser                | 1.16 sec                                                   | 1.18 sec: 1.01x slower                                                           |
| genshi_xml               | 51.6 ms                                                    | 52.5 ms: 1.02x slower                                                            |
| pickle                   | 11.5 us                                                    | 11.7 us: 1.02x slower                                                            |
| logging_simple           | 5.74 us                                                    | 5.90 us: 1.03x slower                                                            |
| genshi_text              | 23.7 ms                                                    | 24.3 ms: 1.03x slower                                                            |
| coverage                 | 93.1 ms                                                    | 97.3 ms: 1.05x slower                                                            |
| tomli_loads              | 2.12 sec                                                   | 2.22 sec: 1.05x slower                                                           |
| unpickle                 | 15.1 us                                                    | 16.2 us: 1.07x slower                                                            |
| pathlib                  | 17.3 ms                                                    | 18.7 ms: 1.08x slower                                                            |
| python_startup_no_site   | 7.11 ms                                                    | 9.03 ms: 1.27x slower                                                            |
| Geometric mean           | (ref)                                                      | 1.02x faster                                                                     |

Benchmark hidden because not significant (19): async_tree_cpu_io_mixed, mypy2, dask, xml_etree_parse, aiohttp, json, logging_format, unpickle_pure_python, gunicorn, async_tree_cpu_io_mixed_tg, bench_mp_pool, tornado_http, async_generators, async_tree_none_tg, asyncio_websockets, async_tree_io_tg, djangocms, async_tree_memoization_tg, async_tree_none
Ignored benchmarks (2) of results/bm-20240605-3.13.0b2-3a83b17/bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17.json: bpe_tokeniser, flaskblogging
Ignored benchmarks (1) of results/bm-20240402-3.13.0a5+-8069375/bm-20240402-linux-x86_64-faster%2dcpython-interpreter_reentry_-3.13.0a5+-8069375.json: unpack_sequence

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.01x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 0.98x