# Results vs. 3.12.0

- fork: faster-cpython
- ref: specialize_binary_op
- machine: linux-x86_64
- commit hash: cd8bea7
- commit date: 2024-04-06
- overall geometric mean: 1.04x faster
- HPT reliability: 99.99%
- HPT 99th percentile: 1.01x faster
- Memory change: 0.96x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240406-linux-x86_64-faster%2dcpython-specialize_binary_op-3.13.0a5+-cd8bea7 |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| 2to3           | 274 ms                                                 | 268 ms: 1.02x faster                                                             |
| chameleon      | 7.41 ms                                                | 6.97 ms: 1.06x faster                                                            |
| docutils       | 2.77 sec                                               | 2.80 sec: 1.01x slower                                                           |
| tornado_http   | 103 ms                                                 | 93.9 ms: 1.09x faster                                                            |
| Geometric mean | (ref)                                                  | 1.04x faster                                                                     |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240406-linux-x86_64-faster%2dcpython-specialize_binary_op-3.13.0a5+-cd8bea7 |
|----------------------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| async_tree_none_tg         | 450 ms                                                 | 334 ms: 1.34x faster                                                             |
| async_tree_none            | 472 ms                                                 | 355 ms: 1.33x faster                                                             |
| async_tree_memoization_tg  | 575 ms                                                 | 441 ms: 1.30x faster                                                             |
| async_tree_io_tg           | 1.18 sec                                               | 926 ms: 1.28x faster                                                             |
| async_tree_memoization     | 578 ms                                                 | 457 ms: 1.26x faster                                                             |
| async_tree_io              | 1.16 sec                                               | 920 ms: 1.26x faster                                                             |
| async_tree_cpu_io_mixed_tg | 726 ms                                                 | 600 ms: 1.21x faster                                                             |
| async_tree_cpu_io_mixed    | 726 ms                                                 | 607 ms: 1.20x faster                                                             |
| Geometric mean             | (ref)                                                  | 1.27x faster                                                                     |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240406-linux-x86_64-faster%2dcpython-specialize_binary_op-3.13.0a5+-cd8bea7 |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| float          | 84.7 ms                                                | 77.6 ms: 1.09x faster                                                            |
| nbody          | 97.0 ms                                                | 94.4 ms: 1.03x faster                                                            |
| pidigits       | 187 ms                                                 | 194 ms: 1.04x slower                                                             |
| Geometric mean | (ref)                                                  | 1.03x faster                                                                     |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240406-linux-x86_64-faster%2dcpython-specialize_binary_op-3.13.0a5+-cd8bea7 |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| regex_compile  | 148 ms                                                 | 135 ms: 1.10x faster                                                             |
| regex_effbot   | 3.61 ms                                                | 3.81 ms: 1.06x slower                                                            |
| regex_dna      | 212 ms                                                 | 230 ms: 1.08x slower                                                             |
| regex_v8       | 23.1 ms                                                | 26.2 ms: 1.13x slower                                                            |
| Geometric mean | (ref)                                                  | 1.04x slower                                                                     |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240406-linux-x86_64-faster%2dcpython-specialize_binary_op-3.13.0a5+-cd8bea7 |
|----------------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| pickle_pure_python   | 324 us                                                 | 302 us: 1.07x faster                                                             |
| unpickle_list        | 5.29 us                                                | 4.98 us: 1.06x faster                                                            |
| tomli_loads          | 2.33 sec                                               | 2.21 sec: 1.06x faster                                                           |
| unpickle_pure_python | 230 us                                                 | 219 us: 1.05x faster                                                             |
| unpickle             | 15.9 us                                                | 15.4 us: 1.03x faster                                                            |
| xml_etree_generate   | 89.2 ms                                                | 86.7 ms: 1.03x faster                                                            |
| xml_etree_process    | 61.7 ms                                                | 60.0 ms: 1.03x faster                                                            |
| json_loads           | 28.5 us                                                | 28.7 us: 1.01x slower                                                            |
| json_dumps           | 10.4 ms                                                | 10.6 ms: 1.02x slower                                                            |
| pickle               | 11.6 us                                                | 11.8 us: 1.02x slower                                                            |
| pickle_list          | 5.08 us                                                | 5.18 us: 1.02x slower                                                            |
| Geometric mean       | (ref)                                                  | 1.02x faster                                                                     |

Benchmark hidden because not significant (3): xml_etree_iterparse, pickle_dict, xml_etree_parse

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240406-linux-x86_64-faster%2dcpython-specialize_binary_op-3.13.0a5+-cd8bea7 |
|------------------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| python_startup         | 9.55 ms                                                | 10.6 ms: 1.11x slower                                                            |
| python_startup_no_site | 6.94 ms                                                | 8.99 ms: 1.30x slower                                                            |
| Geometric mean         | (ref)                                                  | 1.20x slower                                                                     |

Benchmarks with tag 'template':
===============================

| Benchmark | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240406-linux-x86_64-faster%2dcpython-specialize_binary_op-3.13.0a5+-cd8bea7 |
|-----------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| mako      | 11.9 ms                                                | 11.2 ms: 1.06x faster                                                            |

All benchmarks:
===============

| Benchmark                  | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240406-linux-x86_64-faster%2dcpython-specialize_binary_op-3.13.0a5+-cd8bea7 |
|----------------------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| typing_runtime_protocols   | 158 us                                                 | 111 us: 1.42x faster                                                             |
| async_tree_none_tg         | 450 ms                                                 | 334 ms: 1.34x faster                                                             |
| async_tree_none            | 472 ms                                                 | 355 ms: 1.33x faster                                                             |
| async_tree_memoization_tg  | 575 ms                                                 | 441 ms: 1.30x faster                                                             |
| comprehensions             | 21.8 us                                                | 16.7 us: 1.30x faster                                                            |
| async_tree_io_tg           | 1.18 sec                                               | 926 ms: 1.28x faster                                                             |
| async_tree_memoization     | 578 ms                                                 | 457 ms: 1.26x faster                                                             |
| async_tree_io              | 1.16 sec                                               | 920 ms: 1.26x faster                                                             |
| async_tree_cpu_io_mixed_tg | 726 ms                                                 | 600 ms: 1.21x faster                                                             |
| async_tree_cpu_io_mixed    | 726 ms                                                 | 607 ms: 1.20x faster                                                             |
| raytrace                   | 312 ms                                                 | 267 ms: 1.17x faster                                                             |
| crypto_pyaes               | 81.9 ms                                                | 70.9 ms: 1.15x faster                                                            |
| logging_format             | 7.23 us                                                | 6.27 us: 1.15x faster                                                            |
| logging_simple             | 6.46 us                                                | 5.64 us: 1.15x faster                                                            |
| deltablue                  | 3.72 ms                                                | 3.25 ms: 1.14x faster                                                            |
| mypy2                      | 830 ms                                                 | 738 ms: 1.12x faster                                                             |
| regex_compile              | 148 ms                                                 | 135 ms: 1.10x faster                                                             |
| scimark_monte_carlo        | 75.1 ms                                                | 68.4 ms: 1.10x faster                                                            |
| chaos                      | 67.0 ms                                                | 61.2 ms: 1.09x faster                                                            |
| sympy_sum                  | 169 ms                                                 | 155 ms: 1.09x faster                                                             |
| tornado_http               | 103 ms                                                 | 93.9 ms: 1.09x faster                                                            |
| float                      | 84.7 ms                                                | 77.6 ms: 1.09x faster                                                            |
| sympy_str                  | 300 ms                                                 | 278 ms: 1.08x faster                                                             |
| pickle_pure_python         | 324 us                                                 | 302 us: 1.07x faster                                                             |
| spectral_norm              | 115 ms                                                 | 107 ms: 1.07x faster                                                             |
| pyflate                    | 482 ms                                                 | 452 ms: 1.07x faster                                                             |
| deepcopy_memo              | 40.7 us                                                | 38.2 us: 1.07x faster                                                            |
| chameleon                  | 7.41 ms                                                | 6.97 ms: 1.06x faster                                                            |
| unpickle_list              | 5.29 us                                                | 4.98 us: 1.06x faster                                                            |
| mako                       | 11.9 ms                                                | 11.2 ms: 1.06x faster                                                            |
| gc_traversal               | 3.79 ms                                                | 3.57 ms: 1.06x faster                                                            |
| deepcopy_reduce            | 3.35 us                                                | 3.15 us: 1.06x faster                                                            |
| sqlglot_transpile          | 1.68 ms                                                | 1.59 ms: 1.06x faster                                                            |
| tomli_loads                | 2.33 sec                                               | 2.21 sec: 1.06x faster                                                           |
| async_generators           | 463 ms                                                 | 439 ms: 1.05x faster                                                             |
| fannkuch                   | 417 ms                                                 | 396 ms: 1.05x faster                                                             |
| deepcopy                   | 371 us                                                 | 352 us: 1.05x faster                                                             |
| sympy_integrate            | 21.4 ms                                                | 20.3 ms: 1.05x faster                                                            |
| generators                 | 31.2 ms                                                | 29.7 ms: 1.05x faster                                                            |
| unpickle_pure_python       | 230 us                                                 | 219 us: 1.05x faster                                                             |
| sqlglot_parse              | 1.36 ms                                                | 1.30 ms: 1.05x faster                                                            |
| pathlib                    | 19.3 ms                                                | 18.5 ms: 1.05x faster                                                            |
| pprint_safe_repr           | 776 ms                                                 | 741 ms: 1.05x faster                                                             |
| scimark_lu                 | 118 ms                                                 | 114 ms: 1.03x faster                                                             |
| pprint_pformat             | 1.57 sec                                               | 1.52 sec: 1.03x faster                                                           |
| sympy_expand               | 478 ms                                                 | 464 ms: 1.03x faster                                                             |
| meteor_contest             | 112 ms                                                 | 109 ms: 1.03x faster                                                             |
| unpickle                   | 15.9 us                                                | 15.4 us: 1.03x faster                                                            |
| xml_etree_generate         | 89.2 ms                                                | 86.7 ms: 1.03x faster                                                            |
| xml_etree_process          | 61.7 ms                                                | 60.0 ms: 1.03x faster                                                            |
| scimark_sparse_mat_mult    | 5.06 ms                                                | 4.92 ms: 1.03x faster                                                            |
| nbody                      | 97.0 ms                                                | 94.4 ms: 1.03x faster                                                            |
| mdp                        | 2.63 sec                                               | 2.57 sec: 1.03x faster                                                           |
| logging_silent             | 104 ns                                                 | 102 ns: 1.02x faster                                                             |
| hexiom                     | 6.41 ms                                                | 6.27 ms: 1.02x faster                                                            |
| 2to3                       | 274 ms                                                 | 268 ms: 1.02x faster                                                             |
| bench_thread_pool          | 842 us                                                 | 828 us: 1.02x faster                                                             |
| scimark_fft                | 382 ms                                                 | 377 ms: 1.01x faster                                                             |
| nqueens                    | 83.3 ms                                                | 82.5 ms: 1.01x faster                                                            |
| dulwich_log                | 68.5 ms                                                | 67.9 ms: 1.01x faster                                                            |
| bench_mp_pool              | 24.0 ms                                                | 23.8 ms: 1.01x faster                                                            |
| json_loads                 | 28.5 us                                                | 28.7 us: 1.01x slower                                                            |
| docutils                   | 2.77 sec                                               | 2.80 sec: 1.01x slower                                                           |
| aiohttp                    | 1.15 ms                                                | 1.16 ms: 1.01x slower                                                            |
| json_dumps                 | 10.4 ms                                                | 10.6 ms: 1.02x slower                                                            |
| pickle                     | 11.6 us                                                | 11.8 us: 1.02x slower                                                            |
| pycparser                  | 1.18 sec                                               | 1.20 sec: 1.02x slower                                                           |
| gunicorn                   | 1.24 ms                                                | 1.26 ms: 1.02x slower                                                            |
| pickle_list                | 5.08 us                                                | 5.18 us: 1.02x slower                                                            |
| go                         | 139 ms                                                 | 143 ms: 1.03x slower                                                             |
| asyncio_websockets         | 551 ms                                                 | 567 ms: 1.03x slower                                                             |
| richards_super             | 51.5 ms                                                | 53.1 ms: 1.03x slower                                                            |
| json                       | 5.26 ms                                                | 5.42 ms: 1.03x slower                                                            |
| asyncio_tcp                | 491 ms                                                 | 506 ms: 1.03x slower                                                             |
| richards                   | 45.8 ms                                                | 47.3 ms: 1.03x slower                                                            |
| asyncio_tcp_ssl            | 1.79 sec                                               | 1.84 sec: 1.03x slower                                                           |
| pidigits                   | 187 ms                                                 | 194 ms: 1.04x slower                                                             |
| sqlite_synth               | 2.83 us                                                | 2.95 us: 1.04x slower                                                            |
| regex_effbot               | 3.61 ms                                                | 3.81 ms: 1.06x slower                                                            |
| regex_dna                  | 212 ms                                                 | 230 ms: 1.08x slower                                                             |
| python_startup             | 9.55 ms                                                | 10.6 ms: 1.11x slower                                                            |
| regex_v8                   | 23.1 ms                                                | 26.2 ms: 1.13x slower                                                            |
| create_gc_cycles           | 1.48 ms                                                | 1.74 ms: 1.18x slower                                                            |
| telco                      | 7.10 ms                                                | 8.46 ms: 1.19x slower                                                            |
| python_startup_no_site     | 6.94 ms                                                | 8.99 ms: 1.30x slower                                                            |
| coverage                   | 72.7 ms                                                | 97.7 ms: 1.34x slower                                                            |
| Geometric mean             | (ref)                                                  | 1.04x faster                                                                     |

Benchmark hidden because not significant (8): dask, xml_etree_iterparse, pickle_dict, sqlglot_normalize, coroutines, sqlglot_optimize, xml_etree_parse, scimark_sor
Ignored benchmarks (4) of results/bm-20231002-3.12.0-0fb18b0/bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0.json: django_template, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
Ignored benchmarks (5) of results/bm-20240406-3.13.0a5+-cd8bea7/bm-20240406-linux-x86_64-faster%2dcpython-specialize_binary_op-3.13.0a5+-cd8bea7.json: genshi_text, genshi_xml, html5lib, pylint, thrift

# HPT report

- Reliability score: 99.99% likely to be faster
- 90% likely to have a speedup of 1.02x
- 95% likely to have a speedup of 1.01x
- 99% likely to have a speedup of 1.01x

# Memory
- memory change: 0.96x