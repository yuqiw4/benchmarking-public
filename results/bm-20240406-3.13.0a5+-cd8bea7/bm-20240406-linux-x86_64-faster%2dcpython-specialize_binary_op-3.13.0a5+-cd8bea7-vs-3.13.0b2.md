# Results vs. 3.13.0b2

- fork: faster-cpython
- ref: specialize_binary_op
- machine: linux-x86_64
- commit hash: cd8bea7
- commit date: 2024-04-06
- overall geometric mean: 1.01x faster
- HPT reliability: 99.95%
- HPT 99th percentile: 1.00x faster
- Memory change: 0.98x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240406-linux-x86_64-faster%2dcpython-specialize_binary_op-3.13.0a5+-cd8bea7 |
|----------------|:----------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| 2to3           | 274 ms                                                     | 268 ms: 1.02x faster                                                             |
| chameleon      | 7.22 ms                                                    | 6.97 ms: 1.03x faster                                                            |
| docutils       | 2.83 sec                                                   | 2.80 sec: 1.01x faster                                                           |
| html5lib       | 67.2 ms                                                    | 68.2 ms: 1.02x slower                                                            |
| tornado_http   | 94.6 ms                                                    | 93.9 ms: 1.01x faster                                                            |
| Geometric mean | (ref)                                                      | 1.01x faster                                                                     |

Benchmarks with tag 'asyncio':
==============================

| Benchmark       | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240406-linux-x86_64-faster%2dcpython-specialize_binary_op-3.13.0a5+-cd8bea7 |
|-----------------|:----------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| async_tree_none | 378 ms                                                     | 355 ms: 1.07x faster                                                             |
| Geometric mean  | (ref)                                                      | 1.01x faster                                                                     |

Benchmark hidden because not significant (7): async_tree_io, async_tree_memoization, async_tree_io_tg, async_tree_memoization_tg, async_tree_cpu_io_mixed, async_tree_none_tg, async_tree_cpu_io_mixed_tg

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240406-linux-x86_64-faster%2dcpython-specialize_binary_op-3.13.0a5+-cd8bea7 |
|----------------|:----------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| float          | 78.9 ms                                                    | 77.6 ms: 1.02x faster                                                            |
| pidigits       | 191 ms                                                     | 194 ms: 1.01x slower                                                             |
| nbody          | 88.3 ms                                                    | 94.4 ms: 1.07x slower                                                            |
| Geometric mean | (ref)                                                      | 1.02x slower                                                                     |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240406-linux-x86_64-faster%2dcpython-specialize_binary_op-3.13.0a5+-cd8bea7 |
|----------------|:----------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| regex_compile  | 137 ms                                                     | 135 ms: 1.01x faster                                                             |
| regex_dna      | 221 ms                                                     | 230 ms: 1.04x slower                                                             |
| regex_effbot   | 3.67 ms                                                    | 3.81 ms: 1.04x slower                                                            |
| regex_v8       | 25.1 ms                                                    | 26.2 ms: 1.04x slower                                                            |
| Geometric mean | (ref)                                                      | 1.03x slower                                                                     |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240406-linux-x86_64-faster%2dcpython-specialize_binary_op-3.13.0a5+-cd8bea7 |
|----------------------|:----------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| unpickle_list        | 5.34 us                                                    | 4.98 us: 1.07x faster                                                            |
| xml_etree_process    | 61.2 ms                                                    | 60.0 ms: 1.02x faster                                                            |
| json_dumps           | 10.7 ms                                                    | 10.6 ms: 1.02x faster                                                            |
| pickle_pure_python   | 305 us                                                     | 302 us: 1.01x faster                                                             |
| xml_etree_generate   | 87.4 ms                                                    | 86.7 ms: 1.01x faster                                                            |
| xml_etree_iterparse  | 107 ms                                                     | 106 ms: 1.01x faster                                                             |
| json_loads           | 28.9 us                                                    | 28.7 us: 1.01x faster                                                            |
| unpickle_pure_python | 218 us                                                     | 219 us: 1.01x slower                                                             |
| pickle_list          | 5.11 us                                                    | 5.18 us: 1.01x slower                                                            |
| unpickle             | 15.1 us                                                    | 15.4 us: 1.02x slower                                                            |
| pickle_dict          | 34.8 us                                                    | 35.5 us: 1.02x slower                                                            |
| pickle               | 11.5 us                                                    | 11.8 us: 1.03x slower                                                            |
| tomli_loads          | 2.12 sec                                                   | 2.21 sec: 1.04x slower                                                           |
| Geometric mean       | (ref)                                                      | 1.00x faster                                                                     |

Benchmark hidden because not significant (1): xml_etree_parse

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240406-linux-x86_64-faster%2dcpython-specialize_binary_op-3.13.0a5+-cd8bea7 |
|------------------------|:----------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| python_startup         | 10.8 ms                                                    | 10.6 ms: 1.02x faster                                                            |
| python_startup_no_site | 7.11 ms                                                    | 8.99 ms: 1.27x slower                                                            |
| Geometric mean         | (ref)                                                      | 1.11x slower                                                                     |

Benchmarks with tag 'template':
===============================

| Benchmark      | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240406-linux-x86_64-faster%2dcpython-specialize_binary_op-3.13.0a5+-cd8bea7 |
|----------------|:----------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| genshi_text    | 23.7 ms                                                    | 23.5 ms: 1.01x faster                                                            |
| Geometric mean | (ref)                                                      | 1.00x faster                                                                     |

Benchmark hidden because not significant (2): mako, genshi_xml

All benchmarks:
===============

| Benchmark                | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240406-linux-x86_64-faster%2dcpython-specialize_binary_op-3.13.0a5+-cd8bea7 |
|--------------------------|:----------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| typing_runtime_protocols | 165 us                                                     | 111 us: 1.48x faster                                                             |
| pylint                   | 317 ms                                                     | 278 ms: 1.14x faster                                                             |
| gc_traversal             | 3.98 ms                                                    | 3.57 ms: 1.11x faster                                                            |
| crypto_pyaes             | 77.5 ms                                                    | 70.9 ms: 1.09x faster                                                            |
| mdp                      | 2.79 sec                                                   | 2.57 sec: 1.09x faster                                                           |
| spectral_norm            | 116 ms                                                     | 107 ms: 1.09x faster                                                             |
| richards_super           | 57.4 ms                                                    | 53.1 ms: 1.08x faster                                                            |
| richards                 | 50.9 ms                                                    | 47.3 ms: 1.08x faster                                                            |
| unpickle_list            | 5.34 us                                                    | 4.98 us: 1.07x faster                                                            |
| pyflate                  | 484 ms                                                     | 452 ms: 1.07x faster                                                             |
| scimark_sparse_mat_mult  | 5.27 ms                                                    | 4.92 ms: 1.07x faster                                                            |
| async_tree_none          | 378 ms                                                     | 355 ms: 1.07x faster                                                             |
| scimark_lu               | 122 ms                                                     | 114 ms: 1.06x faster                                                             |
| deepcopy_reduce          | 3.35 us                                                    | 3.15 us: 1.06x faster                                                            |
| create_gc_cycles         | 1.82 ms                                                    | 1.74 ms: 1.05x faster                                                            |
| deepcopy                 | 367 us                                                     | 352 us: 1.04x faster                                                             |
| deepcopy_memo            | 39.7 us                                                    | 38.2 us: 1.04x faster                                                            |
| scimark_fft              | 392 ms                                                     | 377 ms: 1.04x faster                                                             |
| chameleon                | 7.22 ms                                                    | 6.97 ms: 1.03x faster                                                            |
| logging_format           | 6.47 us                                                    | 6.27 us: 1.03x faster                                                            |
| logging_silent           | 105 ns                                                     | 102 ns: 1.03x faster                                                             |
| sqlglot_transpile        | 1.63 ms                                                    | 1.59 ms: 1.03x faster                                                            |
| pprint_pformat           | 1.56 sec                                                   | 1.52 sec: 1.02x faster                                                           |
| pprint_safe_repr         | 758 ms                                                     | 741 ms: 1.02x faster                                                             |
| 2to3                     | 274 ms                                                     | 268 ms: 1.02x faster                                                             |
| sympy_expand             | 473 ms                                                     | 464 ms: 1.02x faster                                                             |
| xml_etree_process        | 61.2 ms                                                    | 60.0 ms: 1.02x faster                                                            |
| logging_simple           | 5.74 us                                                    | 5.64 us: 1.02x faster                                                            |
| python_startup           | 10.8 ms                                                    | 10.6 ms: 1.02x faster                                                            |
| json_dumps               | 10.7 ms                                                    | 10.6 ms: 1.02x faster                                                            |
| float                    | 78.9 ms                                                    | 77.6 ms: 1.02x faster                                                            |
| sympy_str                | 282 ms                                                     | 278 ms: 1.02x faster                                                             |
| fannkuch                 | 402 ms                                                     | 396 ms: 1.02x faster                                                             |
| sqlglot_parse            | 1.32 ms                                                    | 1.30 ms: 1.02x faster                                                            |
| aiohttp                  | 1.18 ms                                                    | 1.16 ms: 1.02x faster                                                            |
| regex_compile            | 137 ms                                                     | 135 ms: 1.01x faster                                                             |
| sqlite_synth             | 2.99 us                                                    | 2.95 us: 1.01x faster                                                            |
| pickle_pure_python       | 305 us                                                     | 302 us: 1.01x faster                                                             |
| sqlglot_optimize         | 55.5 ms                                                    | 54.9 ms: 1.01x faster                                                            |
| gunicorn                 | 1.28 ms                                                    | 1.26 ms: 1.01x faster                                                            |
| thrift                   | 823 us                                                     | 814 us: 1.01x faster                                                             |
| scimark_monte_carlo      | 69.2 ms                                                    | 68.4 ms: 1.01x faster                                                            |
| docutils                 | 2.83 sec                                                   | 2.80 sec: 1.01x faster                                                           |
| go                       | 145 ms                                                     | 143 ms: 1.01x faster                                                             |
| xml_etree_generate       | 87.4 ms                                                    | 86.7 ms: 1.01x faster                                                            |
| xml_etree_iterparse      | 107 ms                                                     | 106 ms: 1.01x faster                                                             |
| sympy_integrate          | 20.5 ms                                                    | 20.3 ms: 1.01x faster                                                            |
| json_loads               | 28.9 us                                                    | 28.7 us: 1.01x faster                                                            |
| bench_thread_pool        | 834 us                                                     | 828 us: 1.01x faster                                                             |
| tornado_http             | 94.6 ms                                                    | 93.9 ms: 1.01x faster                                                            |
| sympy_sum                | 156 ms                                                     | 155 ms: 1.01x faster                                                             |
| async_generators         | 442 ms                                                     | 439 ms: 1.01x faster                                                             |
| genshi_text              | 23.7 ms                                                    | 23.5 ms: 1.01x faster                                                            |
| meteor_contest           | 110 ms                                                     | 109 ms: 1.01x faster                                                             |
| hexiom                   | 6.30 ms                                                    | 6.27 ms: 1.00x faster                                                            |
| asyncio_tcp              | 508 ms                                                     | 506 ms: 1.00x faster                                                             |
| comprehensions           | 16.6 us                                                    | 16.7 us: 1.01x slower                                                            |
| unpickle_pure_python     | 218 us                                                     | 219 us: 1.01x slower                                                             |
| dulwich_log              | 67.2 ms                                                    | 67.9 ms: 1.01x slower                                                            |
| pidigits                 | 191 ms                                                     | 194 ms: 1.01x slower                                                             |
| nqueens                  | 81.4 ms                                                    | 82.5 ms: 1.01x slower                                                            |
| pickle_list              | 5.11 us                                                    | 5.18 us: 1.01x slower                                                            |
| html5lib                 | 67.2 ms                                                    | 68.2 ms: 1.02x slower                                                            |
| scimark_sor              | 127 ms                                                     | 130 ms: 1.02x slower                                                             |
| unpickle                 | 15.1 us                                                    | 15.4 us: 1.02x slower                                                            |
| pickle_dict              | 34.8 us                                                    | 35.5 us: 1.02x slower                                                            |
| json                     | 5.31 ms                                                    | 5.42 ms: 1.02x slower                                                            |
| pickle                   | 11.5 us                                                    | 11.8 us: 1.03x slower                                                            |
| pycparser                | 1.16 sec                                                   | 1.20 sec: 1.04x slower                                                           |
| regex_dna                | 221 ms                                                     | 230 ms: 1.04x slower                                                             |
| regex_effbot             | 3.67 ms                                                    | 3.81 ms: 1.04x slower                                                            |
| tomli_loads              | 2.12 sec                                                   | 2.21 sec: 1.04x slower                                                           |
| regex_v8                 | 25.1 ms                                                    | 26.2 ms: 1.04x slower                                                            |
| coverage                 | 93.1 ms                                                    | 97.7 ms: 1.05x slower                                                            |
| pathlib                  | 17.3 ms                                                    | 18.5 ms: 1.07x slower                                                            |
| nbody                    | 88.3 ms                                                    | 94.4 ms: 1.07x slower                                                            |
| python_startup_no_site   | 7.11 ms                                                    | 8.99 ms: 1.27x slower                                                            |
| Geometric mean           | (ref)                                                      | 1.01x faster                                                                     |

Benchmark hidden because not significant (22): async_tree_io, async_tree_memoization, xml_etree_parse, async_tree_io_tg, async_tree_memoization_tg, async_tree_cpu_io_mixed, async_tree_none_tg, mypy2, dask, mako, chaos, bench_mp_pool, deltablue, asyncio_websockets, coroutines, genshi_xml, sqlglot_normalize, asyncio_tcp_ssl, raytrace, generators, telco, async_tree_cpu_io_mixed_tg
Ignored benchmarks (4) of results/bm-20240605-3.13.0b2-3a83b17/bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17.json: bpe_tokeniser, django_template, djangocms, flaskblogging

# HPT report

- Reliability score: 99.95% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 0.98x