# Results vs. 3.13.0b2

- fork: faster-cpython
- ref: specialize_binary_op
- machine: linux-x86_64
- commit hash: 2c964fa
- commit date: 2024-04-05
- overall geometric mean: 1.02x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.00x faster
- Memory change: 0.98x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240405-linux-x86_64-faster%2dcpython-specialize_binary_op-3.13.0a5+-2c964fa |
|----------------|:----------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| 2to3           | 274 ms                                                     | 267 ms: 1.03x faster                                                             |
| chameleon      | 7.22 ms                                                    | 6.93 ms: 1.04x faster                                                            |
| docutils       | 2.83 sec                                                   | 2.79 sec: 1.01x faster                                                           |
| tornado_http   | 94.6 ms                                                    | 94.3 ms: 1.00x faster                                                            |
| Geometric mean | (ref)                                                      | 1.02x faster                                                                     |

Benchmark hidden because not significant (1): html5lib

Benchmarks with tag 'asyncio':
==============================

| Benchmark       | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240405-linux-x86_64-faster%2dcpython-specialize_binary_op-3.13.0a5+-2c964fa |
|-----------------|:----------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| async_tree_none | 378 ms                                                     | 351 ms: 1.08x faster                                                             |
| async_tree_io   | 939 ms                                                     | 912 ms: 1.03x faster                                                             |
| Geometric mean  | (ref)                                                      | 1.01x faster                                                                     |

Benchmark hidden because not significant (6): async_tree_cpu_io_mixed, async_tree_memoization, async_tree_none_tg, async_tree_io_tg, async_tree_memoization_tg, async_tree_cpu_io_mixed_tg

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240405-linux-x86_64-faster%2dcpython-specialize_binary_op-3.13.0a5+-2c964fa |
|----------------|:----------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| float          | 78.9 ms                                                    | 78.2 ms: 1.01x faster                                                            |
| nbody          | 88.3 ms                                                    | 95.9 ms: 1.09x slower                                                            |
| pidigits       | 191 ms                                                     | 216 ms: 1.13x slower                                                             |
| Geometric mean | (ref)                                                      | 1.07x slower                                                                     |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240405-linux-x86_64-faster%2dcpython-specialize_binary_op-3.13.0a5+-2c964fa |
|----------------|:----------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| regex_v8       | 25.1 ms                                                    | 24.4 ms: 1.03x faster                                                            |
| regex_compile  | 137 ms                                                     | 135 ms: 1.01x faster                                                             |
| regex_dna      | 221 ms                                                     | 218 ms: 1.01x faster                                                             |
| regex_effbot   | 3.67 ms                                                    | 3.69 ms: 1.00x slower                                                            |
| Geometric mean | (ref)                                                      | 1.01x faster                                                                     |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240405-linux-x86_64-faster%2dcpython-specialize_binary_op-3.13.0a5+-2c964fa |
|----------------------|:----------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| unpickle_list        | 5.34 us                                                    | 5.11 us: 1.04x faster                                                            |
| pickle_list          | 5.11 us                                                    | 4.93 us: 1.04x faster                                                            |
| json_dumps           | 10.7 ms                                                    | 10.5 ms: 1.02x faster                                                            |
| xml_etree_process    | 61.2 ms                                                    | 59.8 ms: 1.02x faster                                                            |
| json_loads           | 28.9 us                                                    | 28.5 us: 1.01x faster                                                            |
| xml_etree_generate   | 87.4 ms                                                    | 86.7 ms: 1.01x faster                                                            |
| unpickle             | 15.1 us                                                    | 15.0 us: 1.01x faster                                                            |
| unpickle_pure_python | 218 us                                                     | 221 us: 1.01x slower                                                             |
| pickle_dict          | 34.8 us                                                    | 35.3 us: 1.01x slower                                                            |
| pickle               | 11.5 us                                                    | 11.7 us: 1.02x slower                                                            |
| tomli_loads          | 2.12 sec                                                   | 2.19 sec: 1.03x slower                                                           |
| Geometric mean       | (ref)                                                      | 1.01x faster                                                                     |

Benchmark hidden because not significant (3): xml_etree_parse, xml_etree_iterparse, pickle_pure_python

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240405-linux-x86_64-faster%2dcpython-specialize_binary_op-3.13.0a5+-2c964fa |
|------------------------|:----------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| python_startup         | 10.8 ms                                                    | 10.5 ms: 1.02x faster                                                            |
| python_startup_no_site | 7.11 ms                                                    | 8.97 ms: 1.26x slower                                                            |
| Geometric mean         | (ref)                                                      | 1.11x slower                                                                     |

Benchmarks with tag 'template':
===============================

| Benchmark      | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240405-linux-x86_64-faster%2dcpython-specialize_binary_op-3.13.0a5+-2c964fa |
|----------------|:----------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| mako           | 11.2 ms                                                    | 10.7 ms: 1.05x faster                                                            |
| genshi_xml     | 51.6 ms                                                    | 52.4 ms: 1.02x slower                                                            |
| Geometric mean | (ref)                                                      | 1.01x faster                                                                     |

Benchmark hidden because not significant (1): genshi_text

All benchmarks:
===============

| Benchmark                | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240405-linux-x86_64-faster%2dcpython-specialize_binary_op-3.13.0a5+-2c964fa |
|--------------------------|:----------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| typing_runtime_protocols | 165 us                                                     | 114 us: 1.44x faster                                                             |
| pylint                   | 317 ms                                                     | 277 ms: 1.14x faster                                                             |
| spectral_norm            | 116 ms                                                     | 103 ms: 1.13x faster                                                             |
| crypto_pyaes             | 77.5 ms                                                    | 69.9 ms: 1.11x faster                                                            |
| richards_super           | 57.4 ms                                                    | 52.7 ms: 1.09x faster                                                            |
| richards                 | 50.9 ms                                                    | 47.0 ms: 1.08x faster                                                            |
| mdp                      | 2.79 sec                                                   | 2.58 sec: 1.08x faster                                                           |
| scimark_sparse_mat_mult  | 5.27 ms                                                    | 4.87 ms: 1.08x faster                                                            |
| async_tree_none          | 378 ms                                                     | 351 ms: 1.08x faster                                                             |
| scimark_lu               | 122 ms                                                     | 113 ms: 1.08x faster                                                             |
| deepcopy_reduce          | 3.35 us                                                    | 3.14 us: 1.07x faster                                                            |
| mako                     | 11.2 ms                                                    | 10.7 ms: 1.05x faster                                                            |
| scimark_sor              | 127 ms                                                     | 122 ms: 1.05x faster                                                             |
| scimark_fft              | 392 ms                                                     | 375 ms: 1.05x faster                                                             |
| unpickle_list            | 5.34 us                                                    | 5.11 us: 1.04x faster                                                            |
| deepcopy                 | 367 us                                                     | 352 us: 1.04x faster                                                             |
| chameleon                | 7.22 ms                                                    | 6.93 ms: 1.04x faster                                                            |
| pickle_list              | 5.11 us                                                    | 4.93 us: 1.04x faster                                                            |
| deepcopy_memo            | 39.7 us                                                    | 38.4 us: 1.03x faster                                                            |
| pyflate                  | 484 ms                                                     | 469 ms: 1.03x faster                                                             |
| pprint_pformat           | 1.56 sec                                                   | 1.51 sec: 1.03x faster                                                           |
| regex_v8                 | 25.1 ms                                                    | 24.4 ms: 1.03x faster                                                            |
| create_gc_cycles         | 1.82 ms                                                    | 1.76 ms: 1.03x faster                                                            |
| async_tree_io            | 939 ms                                                     | 912 ms: 1.03x faster                                                             |
| sqlglot_transpile        | 1.63 ms                                                    | 1.59 ms: 1.03x faster                                                            |
| 2to3                     | 274 ms                                                     | 267 ms: 1.03x faster                                                             |
| pprint_safe_repr         | 758 ms                                                     | 739 ms: 1.03x faster                                                             |
| sqlite_synth             | 2.99 us                                                    | 2.92 us: 1.03x faster                                                            |
| json_dumps               | 10.7 ms                                                    | 10.5 ms: 1.02x faster                                                            |
| xml_etree_process        | 61.2 ms                                                    | 59.8 ms: 1.02x faster                                                            |
| sqlglot_parse            | 1.32 ms                                                    | 1.29 ms: 1.02x faster                                                            |
| thrift                   | 823 us                                                     | 806 us: 1.02x faster                                                             |
| python_startup           | 10.8 ms                                                    | 10.5 ms: 1.02x faster                                                            |
| gunicorn                 | 1.28 ms                                                    | 1.26 ms: 1.02x faster                                                            |
| sympy_expand             | 473 ms                                                     | 465 ms: 1.02x faster                                                             |
| pycparser                | 1.16 sec                                                   | 1.14 sec: 1.02x faster                                                           |
| regex_compile            | 137 ms                                                     | 135 ms: 1.01x faster                                                             |
| regex_dna                | 221 ms                                                     | 218 ms: 1.01x faster                                                             |
| docutils                 | 2.83 sec                                                   | 2.79 sec: 1.01x faster                                                           |
| json_loads               | 28.9 us                                                    | 28.5 us: 1.01x faster                                                            |
| aiohttp                  | 1.18 ms                                                    | 1.17 ms: 1.01x faster                                                            |
| sympy_str                | 282 ms                                                     | 279 ms: 1.01x faster                                                             |
| generators               | 29.6 ms                                                    | 29.3 ms: 1.01x faster                                                            |
| fannkuch                 | 402 ms                                                     | 397 ms: 1.01x faster                                                             |
| coroutines               | 23.2 ms                                                    | 22.9 ms: 1.01x faster                                                            |
| sympy_integrate          | 20.5 ms                                                    | 20.3 ms: 1.01x faster                                                            |
| deltablue                | 3.25 ms                                                    | 3.22 ms: 1.01x faster                                                            |
| sympy_sum                | 156 ms                                                     | 154 ms: 1.01x faster                                                             |
| float                    | 78.9 ms                                                    | 78.2 ms: 1.01x faster                                                            |
| xml_etree_generate       | 87.4 ms                                                    | 86.7 ms: 1.01x faster                                                            |
| bench_thread_pool        | 834 us                                                     | 827 us: 1.01x faster                                                             |
| unpickle                 | 15.1 us                                                    | 15.0 us: 1.01x faster                                                            |
| sqlglot_optimize         | 55.5 ms                                                    | 55.1 ms: 1.01x faster                                                            |
| meteor_contest           | 110 ms                                                     | 109 ms: 1.01x faster                                                             |
| asyncio_websockets       | 567 ms                                                     | 563 ms: 1.01x faster                                                             |
| raytrace                 | 267 ms                                                     | 265 ms: 1.01x faster                                                             |
| async_generators         | 442 ms                                                     | 440 ms: 1.01x faster                                                             |
| nqueens                  | 81.4 ms                                                    | 81.0 ms: 1.00x faster                                                            |
| asyncio_tcp              | 508 ms                                                     | 506 ms: 1.00x faster                                                             |
| go                       | 145 ms                                                     | 144 ms: 1.00x faster                                                             |
| tornado_http             | 94.6 ms                                                    | 94.3 ms: 1.00x faster                                                            |
| gc_traversal             | 3.98 ms                                                    | 3.97 ms: 1.00x faster                                                            |
| asyncio_tcp_ssl          | 1.84 sec                                                   | 1.84 sec: 1.00x slower                                                           |
| regex_effbot             | 3.67 ms                                                    | 3.69 ms: 1.00x slower                                                            |
| logging_simple           | 5.74 us                                                    | 5.81 us: 1.01x slower                                                            |
| unpickle_pure_python     | 218 us                                                     | 221 us: 1.01x slower                                                             |
| comprehensions           | 16.6 us                                                    | 16.8 us: 1.01x slower                                                            |
| pickle_dict              | 34.8 us                                                    | 35.3 us: 1.01x slower                                                            |
| genshi_xml               | 51.6 ms                                                    | 52.4 ms: 1.02x slower                                                            |
| sqlglot_normalize        | 110 ms                                                     | 112 ms: 1.02x slower                                                             |
| scimark_monte_carlo      | 69.2 ms                                                    | 70.3 ms: 1.02x slower                                                            |
| pickle                   | 11.5 us                                                    | 11.7 us: 1.02x slower                                                            |
| chaos                    | 61.3 ms                                                    | 62.8 ms: 1.02x slower                                                            |
| json                     | 5.31 ms                                                    | 5.45 ms: 1.03x slower                                                            |
| tomli_loads              | 2.12 sec                                                   | 2.19 sec: 1.03x slower                                                           |
| coverage                 | 93.1 ms                                                    | 98.2 ms: 1.05x slower                                                            |
| pathlib                  | 17.3 ms                                                    | 18.8 ms: 1.08x slower                                                            |
| nbody                    | 88.3 ms                                                    | 95.9 ms: 1.09x slower                                                            |
| pidigits                 | 191 ms                                                     | 216 ms: 1.13x slower                                                             |
| python_startup_no_site   | 7.11 ms                                                    | 8.97 ms: 1.26x slower                                                            |
| Geometric mean           | (ref)                                                      | 1.02x faster                                                                     |

Benchmark hidden because not significant (19): mypy2, async_tree_cpu_io_mixed, xml_etree_parse, dask, async_tree_memoization, xml_etree_iterparse, async_tree_none_tg, async_tree_io_tg, pickle_pure_python, bench_mp_pool, async_tree_memoization_tg, logging_format, html5lib, hexiom, logging_silent, dulwich_log, telco, genshi_text, async_tree_cpu_io_mixed_tg
Ignored benchmarks (4) of results/bm-20240605-3.13.0b2-3a83b17/bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17.json: bpe_tokeniser, django_template, djangocms, flaskblogging

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 0.98x