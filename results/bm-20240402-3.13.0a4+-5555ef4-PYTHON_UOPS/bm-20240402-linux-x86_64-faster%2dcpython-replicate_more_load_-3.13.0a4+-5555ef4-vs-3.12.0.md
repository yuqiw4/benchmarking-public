# Results vs. 3.12.0

- fork: faster-cpython
- ref: replicate_more_load_
- machine: linux-x86_64
- commit hash: 5555ef4
- commit date: 2024-04-02
- overall geometric mean: 1.07x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.04x slower
- Memory change: 0.94x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240402-linux-x86_64-faster%2dcpython-replicate_more_load_-3.13.0a4+-5555ef4 |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| 2to3           | 274 ms                                                 | 300 ms: 1.09x slower                                                             |
| chameleon      | 7.41 ms                                                | 7.08 ms: 1.05x faster                                                            |
| docutils       | 2.77 sec                                               | 2.87 sec: 1.04x slower                                                           |
| Geometric mean | (ref)                                                  | 1.02x slower                                                                     |

Benchmark hidden because not significant (1): tornado_http

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240402-linux-x86_64-faster%2dcpython-replicate_more_load_-3.13.0a4+-5555ef4 |
|----------------------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| async_tree_none            | 472 ms                                                 | 463 ms: 1.02x faster                                                             |
| async_tree_memoization     | 578 ms                                                 | 594 ms: 1.03x slower                                                             |
| async_tree_cpu_io_mixed    | 726 ms                                                 | 747 ms: 1.03x slower                                                             |
| async_tree_cpu_io_mixed_tg | 726 ms                                                 | 754 ms: 1.04x slower                                                             |
| async_tree_none_tg         | 450 ms                                                 | 471 ms: 1.05x slower                                                             |
| async_tree_memoization_tg  | 575 ms                                                 | 603 ms: 1.05x slower                                                             |
| async_tree_io_tg           | 1.18 sec                                               | 1.26 sec: 1.07x slower                                                           |
| async_tree_io              | 1.16 sec                                               | 1.24 sec: 1.07x slower                                                           |
| Geometric mean             | (ref)                                                  | 1.04x slower                                                                     |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240402-linux-x86_64-faster%2dcpython-replicate_more_load_-3.13.0a4+-5555ef4 |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| pidigits       | 187 ms                                                 | 191 ms: 1.02x slower                                                             |
| float          | 84.7 ms                                                | 94.7 ms: 1.12x slower                                                            |
| nbody          | 97.0 ms                                                | 123 ms: 1.27x slower                                                             |
| Geometric mean | (ref)                                                  | 1.13x slower                                                                     |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240402-linux-x86_64-faster%2dcpython-replicate_more_load_-3.13.0a4+-5555ef4 |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| regex_effbot   | 3.61 ms                                                | 3.55 ms: 1.02x faster                                                            |
| regex_dna      | 212 ms                                                 | 213 ms: 1.00x slower                                                             |
| regex_v8       | 23.1 ms                                                | 25.1 ms: 1.08x slower                                                            |
| regex_compile  | 148 ms                                                 | 178 ms: 1.20x slower                                                             |
| Geometric mean | (ref)                                                  | 1.06x slower                                                                     |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240402-linux-x86_64-faster%2dcpython-replicate_more_load_-3.13.0a4+-5555ef4 |
|----------------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| unpickle_list        | 5.29 us                                                | 5.12 us: 1.03x faster                                                            |
| pickle_pure_python   | 324 us                                                 | 314 us: 1.03x faster                                                             |
| unpickle             | 15.9 us                                                | 15.4 us: 1.03x faster                                                            |
| pickle_dict          | 35.5 us                                                | 34.9 us: 1.02x faster                                                            |
| json_loads           | 28.5 us                                                | 28.4 us: 1.01x faster                                                            |
| xml_etree_parse      | 159 ms                                                 | 161 ms: 1.01x slower                                                             |
| xml_etree_process    | 61.7 ms                                                | 62.8 ms: 1.02x slower                                                            |
| xml_etree_generate   | 89.2 ms                                                | 91.6 ms: 1.03x slower                                                            |
| json_dumps           | 10.4 ms                                                | 10.7 ms: 1.03x slower                                                            |
| pickle               | 11.6 us                                                | 12.0 us: 1.03x slower                                                            |
| pickle_list          | 5.08 us                                                | 5.25 us: 1.03x slower                                                            |
| xml_etree_iterparse  | 107 ms                                                 | 113 ms: 1.05x slower                                                             |
| tomli_loads          | 2.33 sec                                               | 2.53 sec: 1.09x slower                                                           |
| unpickle_pure_python | 230 us                                                 | 278 us: 1.21x slower                                                             |
| Geometric mean       | (ref)                                                  | 1.03x slower                                                                     |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240402-linux-x86_64-faster%2dcpython-replicate_more_load_-3.13.0a4+-5555ef4 |
|------------------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| python_startup         | 9.55 ms                                                | 10.5 ms: 1.10x slower                                                            |
| python_startup_no_site | 6.94 ms                                                | 9.07 ms: 1.31x slower                                                            |
| Geometric mean         | (ref)                                                  | 1.20x slower                                                                     |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240402-linux-x86_64-faster%2dcpython-replicate_more_load_-3.13.0a4+-5555ef4 |
|-----------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| django_template | 34.6 ms                                                | 34.5 ms: 1.00x faster                                                            |
| mako            | 11.9 ms                                                | 12.9 ms: 1.08x slower                                                            |
| Geometric mean  | (ref)                                                  | 1.04x slower                                                                     |

All benchmarks:
===============

| Benchmark                  | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240402-linux-x86_64-faster%2dcpython-replicate_more_load_-3.13.0a4+-5555ef4 |
|----------------------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| typing_runtime_protocols   | 158 us                                                 | 118 us: 1.34x faster                                                             |
| deepcopy_reduce            | 3.35 us                                                | 3.11 us: 1.07x faster                                                            |
| chameleon                  | 7.41 ms                                                | 7.08 ms: 1.05x faster                                                            |
| comprehensions             | 21.8 us                                                | 20.9 us: 1.04x faster                                                            |
| unpickle_list              | 5.29 us                                                | 5.12 us: 1.03x faster                                                            |
| pickle_pure_python         | 324 us                                                 | 314 us: 1.03x faster                                                             |
| unpickle                   | 15.9 us                                                | 15.4 us: 1.03x faster                                                            |
| generators                 | 31.2 ms                                                | 30.4 ms: 1.03x faster                                                            |
| async_tree_none            | 472 ms                                                 | 463 ms: 1.02x faster                                                             |
| pickle_dict                | 35.5 us                                                | 34.9 us: 1.02x faster                                                            |
| regex_effbot               | 3.61 ms                                                | 3.55 ms: 1.02x faster                                                            |
| sympy_sum                  | 169 ms                                                 | 166 ms: 1.02x faster                                                             |
| logging_simple             | 6.46 us                                                | 6.37 us: 1.01x faster                                                            |
| deepcopy                   | 371 us                                                 | 367 us: 1.01x faster                                                             |
| logging_format             | 7.23 us                                                | 7.19 us: 1.01x faster                                                            |
| json_loads                 | 28.5 us                                                | 28.4 us: 1.01x faster                                                            |
| django_template            | 34.6 ms                                                | 34.5 ms: 1.00x faster                                                            |
| bench_mp_pool              | 24.0 ms                                                | 23.9 ms: 1.00x faster                                                            |
| logging_silent             | 104 ns                                                 | 104 ns: 1.00x faster                                                             |
| regex_dna                  | 212 ms                                                 | 213 ms: 1.00x slower                                                             |
| sympy_integrate            | 21.4 ms                                                | 21.5 ms: 1.01x slower                                                            |
| xml_etree_parse            | 159 ms                                                 | 161 ms: 1.01x slower                                                             |
| gc_traversal               | 3.79 ms                                                | 3.85 ms: 1.01x slower                                                            |
| xml_etree_process          | 61.7 ms                                                | 62.8 ms: 1.02x slower                                                            |
| json                       | 5.26 ms                                                | 5.35 ms: 1.02x slower                                                            |
| pidigits                   | 187 ms                                                 | 191 ms: 1.02x slower                                                             |
| dask                       | 372 ms                                                 | 379 ms: 1.02x slower                                                             |
| sympy_str                  | 300 ms                                                 | 306 ms: 1.02x slower                                                             |
| asyncio_websockets         | 551 ms                                                 | 564 ms: 1.02x slower                                                             |
| xml_etree_generate         | 89.2 ms                                                | 91.6 ms: 1.03x slower                                                            |
| sqlglot_normalize          | 110 ms                                                 | 113 ms: 1.03x slower                                                             |
| json_dumps                 | 10.4 ms                                                | 10.7 ms: 1.03x slower                                                            |
| async_tree_memoization     | 578 ms                                                 | 594 ms: 1.03x slower                                                             |
| async_tree_cpu_io_mixed    | 726 ms                                                 | 747 ms: 1.03x slower                                                             |
| pickle                     | 11.6 us                                                | 12.0 us: 1.03x slower                                                            |
| pickle_list                | 5.08 us                                                | 5.25 us: 1.03x slower                                                            |
| deepcopy_memo              | 40.7 us                                                | 42.2 us: 1.04x slower                                                            |
| coroutines                 | 23.2 ms                                                | 24.0 ms: 1.04x slower                                                            |
| bench_thread_pool          | 842 us                                                 | 873 us: 1.04x slower                                                             |
| async_generators           | 463 ms                                                 | 480 ms: 1.04x slower                                                             |
| docutils                   | 2.77 sec                                               | 2.87 sec: 1.04x slower                                                           |
| asyncio_tcp                | 491 ms                                                 | 510 ms: 1.04x slower                                                             |
| unpack_sequence            | 54.0 ns                                                | 56.1 ns: 1.04x slower                                                            |
| asyncio_tcp_ssl            | 1.79 sec                                               | 1.86 sec: 1.04x slower                                                           |
| async_tree_cpu_io_mixed_tg | 726 ms                                                 | 754 ms: 1.04x slower                                                             |
| sqlite_synth               | 2.83 us                                                | 2.95 us: 1.04x slower                                                            |
| crypto_pyaes               | 81.9 ms                                                | 85.4 ms: 1.04x slower                                                            |
| meteor_contest             | 112 ms                                                 | 117 ms: 1.04x slower                                                             |
| deltablue                  | 3.72 ms                                                | 3.88 ms: 1.04x slower                                                            |
| mdp                        | 2.63 sec                                               | 2.75 sec: 1.05x slower                                                           |
| async_tree_none_tg         | 450 ms                                                 | 471 ms: 1.05x slower                                                             |
| create_gc_cycles           | 1.48 ms                                                | 1.55 ms: 1.05x slower                                                            |
| async_tree_memoization_tg  | 575 ms                                                 | 603 ms: 1.05x slower                                                             |
| xml_etree_iterparse        | 107 ms                                                 | 113 ms: 1.05x slower                                                             |
| gunicorn                   | 1.24 ms                                                | 1.31 ms: 1.06x slower                                                            |
| aiohttp                    | 1.15 ms                                                | 1.22 ms: 1.06x slower                                                            |
| async_tree_io_tg           | 1.18 sec                                               | 1.26 sec: 1.07x slower                                                           |
| async_tree_io              | 1.16 sec                                               | 1.24 sec: 1.07x slower                                                           |
| dulwich_log                | 68.5 ms                                                | 73.7 ms: 1.08x slower                                                            |
| sqlglot_transpile          | 1.68 ms                                                | 1.81 ms: 1.08x slower                                                            |
| sympy_expand               | 478 ms                                                 | 514 ms: 1.08x slower                                                             |
| sqlglot_parse              | 1.36 ms                                                | 1.47 ms: 1.08x slower                                                            |
| mako                       | 11.9 ms                                                | 12.9 ms: 1.08x slower                                                            |
| regex_v8                   | 23.1 ms                                                | 25.1 ms: 1.08x slower                                                            |
| tomli_loads                | 2.33 sec                                               | 2.53 sec: 1.09x slower                                                           |
| 2to3                       | 274 ms                                                 | 300 ms: 1.09x slower                                                             |
| python_startup             | 9.55 ms                                                | 10.5 ms: 1.10x slower                                                            |
| mypy2                      | 830 ms                                                 | 918 ms: 1.11x slower                                                             |
| raytrace                   | 312 ms                                                 | 346 ms: 1.11x slower                                                             |
| pprint_safe_repr           | 776 ms                                                 | 866 ms: 1.12x slower                                                             |
| sqlglot_optimize           | 54.8 ms                                                | 61.2 ms: 1.12x slower                                                            |
| float                      | 84.7 ms                                                | 94.7 ms: 1.12x slower                                                            |
| chaos                      | 67.0 ms                                                | 75.2 ms: 1.12x slower                                                            |
| pycparser                  | 1.18 sec                                               | 1.33 sec: 1.13x slower                                                           |
| scimark_monte_carlo        | 75.1 ms                                                | 85.9 ms: 1.14x slower                                                            |
| fannkuch                   | 417 ms                                                 | 480 ms: 1.15x slower                                                             |
| pprint_pformat             | 1.57 sec                                               | 1.82 sec: 1.16x slower                                                           |
| scimark_fft                | 382 ms                                                 | 450 ms: 1.18x slower                                                             |
| scimark_sor                | 129 ms                                                 | 154 ms: 1.19x slower                                                             |
| regex_compile              | 148 ms                                                 | 178 ms: 1.20x slower                                                             |
| unpickle_pure_python       | 230 us                                                 | 278 us: 1.21x slower                                                             |
| spectral_norm              | 115 ms                                                 | 140 ms: 1.21x slower                                                             |
| nqueens                    | 83.3 ms                                                | 101 ms: 1.22x slower                                                             |
| richards_super             | 51.5 ms                                                | 63.0 ms: 1.22x slower                                                            |
| scimark_sparse_mat_mult    | 5.06 ms                                                | 6.20 ms: 1.23x slower                                                            |
| richards                   | 45.8 ms                                                | 56.3 ms: 1.23x slower                                                            |
| pyflate                    | 482 ms                                                 | 593 ms: 1.23x slower                                                             |
| telco                      | 7.10 ms                                                | 8.85 ms: 1.25x slower                                                            |
| nbody                      | 97.0 ms                                                | 123 ms: 1.27x slower                                                             |
| go                         | 139 ms                                                 | 179 ms: 1.28x slower                                                             |
| python_startup_no_site     | 6.94 ms                                                | 9.07 ms: 1.31x slower                                                            |
| coverage                   | 72.7 ms                                                | 97.8 ms: 1.35x slower                                                            |
| scimark_lu                 | 118 ms                                                 | 160 ms: 1.36x slower                                                             |
| hexiom                     | 6.41 ms                                                | 9.07 ms: 1.41x slower                                                            |
| Geometric mean             | (ref)                                                  | 1.07x slower                                                                     |

Benchmark hidden because not significant (2): pathlib, tornado_http
Ignored benchmarks (2) of results/bm-20231002-3.12.0-0fb18b0/bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0.json: sqlalchemy_declarative, sqlalchemy_imperative
Ignored benchmarks (6) of results/bm-20240402-3.13.0a4+-5555ef4-PYTHON_UOPS/bm-20240402-linux-x86_64-faster%2dcpython-replicate_more_load_-3.13.0a4+-5555ef4.json: djangocms, genshi_text, genshi_xml, html5lib, pylint, thrift

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.04x
- 95% likely to have a slowdown of 1.04x
- 99% likely to have a slowdown of 1.04x

# Memory
- memory change: 0.94x