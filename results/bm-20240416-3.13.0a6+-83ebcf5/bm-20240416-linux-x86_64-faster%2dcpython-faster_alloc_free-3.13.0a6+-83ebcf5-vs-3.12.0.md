# Results vs. 3.12.0

- fork: faster-cpython
- ref: faster_alloc_free
- machine: linux-x86_64
- commit hash: 83ebcf5
- commit date: 2024-04-16
- overall geometric mean: 1.04x faster
- HPT reliability: 99.43%
- HPT 99th percentile: 1.00x faster
- Memory change: 0.96x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240416-linux-x86_64-faster%2dcpython-faster_alloc_free-3.13.0a6+-83ebcf5 |
|----------------|:------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| 2to3           | 274 ms                                                 | 271 ms: 1.01x faster                                                          |
| chameleon      | 7.41 ms                                                | 7.07 ms: 1.05x faster                                                         |
| docutils       | 2.77 sec                                               | 2.84 sec: 1.03x slower                                                        |
| tornado_http   | 103 ms                                                 | 94.1 ms: 1.09x faster                                                         |
| Geometric mean | (ref)                                                  | 1.03x faster                                                                  |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240416-linux-x86_64-faster%2dcpython-faster_alloc_free-3.13.0a6+-83ebcf5 |
|----------------------------|:------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| async_tree_none_tg         | 450 ms                                                 | 337 ms: 1.33x faster                                                          |
| async_tree_none            | 472 ms                                                 | 357 ms: 1.32x faster                                                          |
| async_tree_memoization_tg  | 575 ms                                                 | 445 ms: 1.29x faster                                                          |
| async_tree_io_tg           | 1.18 sec                                               | 938 ms: 1.26x faster                                                          |
| async_tree_io              | 1.16 sec                                               | 925 ms: 1.25x faster                                                          |
| async_tree_memoization     | 578 ms                                                 | 465 ms: 1.24x faster                                                          |
| async_tree_cpu_io_mixed_tg | 726 ms                                                 | 604 ms: 1.20x faster                                                          |
| async_tree_cpu_io_mixed    | 726 ms                                                 | 607 ms: 1.20x faster                                                          |
| Geometric mean             | (ref)                                                  | 1.26x faster                                                                  |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240416-linux-x86_64-faster%2dcpython-faster_alloc_free-3.13.0a6+-83ebcf5 |
|----------------|:------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| nbody          | 97.0 ms                                                | 90.3 ms: 1.07x faster                                                         |
| float          | 84.7 ms                                                | 79.8 ms: 1.06x faster                                                         |
| pidigits       | 187 ms                                                 | 190 ms: 1.01x slower                                                          |
| Geometric mean | (ref)                                                  | 1.04x faster                                                                  |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240416-linux-x86_64-faster%2dcpython-faster_alloc_free-3.13.0a6+-83ebcf5 |
|----------------|:------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| regex_compile  | 148 ms                                                 | 137 ms: 1.08x faster                                                          |
| regex_effbot   | 3.61 ms                                                | 3.65 ms: 1.01x slower                                                         |
| regex_dna      | 212 ms                                                 | 226 ms: 1.06x slower                                                          |
| regex_v8       | 23.1 ms                                                | 24.8 ms: 1.07x slower                                                         |
| Geometric mean | (ref)                                                  | 1.02x slower                                                                  |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240416-linux-x86_64-faster%2dcpython-faster_alloc_free-3.13.0a6+-83ebcf5 |
|----------------------|:------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| pickle_pure_python   | 324 us                                                 | 302 us: 1.07x faster                                                          |
| unpickle_list        | 5.29 us                                                | 4.98 us: 1.06x faster                                                         |
| pickle_dict          | 35.5 us                                                | 33.9 us: 1.05x faster                                                         |
| tomli_loads          | 2.33 sec                                               | 2.22 sec: 1.05x faster                                                        |
| unpickle             | 15.9 us                                                | 15.1 us: 1.05x faster                                                         |
| unpickle_pure_python | 230 us                                                 | 223 us: 1.03x faster                                                          |
| json_loads           | 28.5 us                                                | 28.0 us: 1.02x faster                                                         |
| pickle_list          | 5.08 us                                                | 5.03 us: 1.01x faster                                                         |
| xml_etree_process    | 61.7 ms                                                | 61.2 ms: 1.01x faster                                                         |
| pickle               | 11.6 us                                                | 11.5 us: 1.01x faster                                                         |
| xml_etree_generate   | 89.2 ms                                                | 88.5 ms: 1.01x faster                                                         |
| xml_etree_iterparse  | 107 ms                                                 | 108 ms: 1.01x slower                                                          |
| json_dumps           | 10.4 ms                                                | 10.6 ms: 1.02x slower                                                         |
| Geometric mean       | (ref)                                                  | 1.02x faster                                                                  |

Benchmark hidden because not significant (1): xml_etree_parse

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240416-linux-x86_64-faster%2dcpython-faster_alloc_free-3.13.0a6+-83ebcf5 |
|------------------------|:------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| python_startup_no_site | 6.94 ms                                                | 7.09 ms: 1.02x slower                                                         |
| python_startup         | 9.55 ms                                                | 10.5 ms: 1.10x slower                                                         |
| Geometric mean         | (ref)                                                  | 1.06x slower                                                                  |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240416-linux-x86_64-faster%2dcpython-faster_alloc_free-3.13.0a6+-83ebcf5 |
|-----------------|:------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| mako            | 11.9 ms                                                | 11.0 ms: 1.09x faster                                                         |
| django_template | 34.6 ms                                                | 35.6 ms: 1.03x slower                                                         |
| Geometric mean  | (ref)                                                  | 1.03x faster                                                                  |

All benchmarks:
===============

| Benchmark                  | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240416-linux-x86_64-faster%2dcpython-faster_alloc_free-3.13.0a6+-83ebcf5 |
|----------------------------|:------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| typing_runtime_protocols   | 158 us                                                 | 113 us: 1.40x faster                                                          |
| async_tree_none_tg         | 450 ms                                                 | 337 ms: 1.33x faster                                                          |
| async_tree_none            | 472 ms                                                 | 357 ms: 1.32x faster                                                          |
| async_tree_memoization_tg  | 575 ms                                                 | 445 ms: 1.29x faster                                                          |
| comprehensions             | 21.8 us                                                | 17.2 us: 1.26x faster                                                         |
| async_tree_io_tg           | 1.18 sec                                               | 938 ms: 1.26x faster                                                          |
| async_tree_io              | 1.16 sec                                               | 925 ms: 1.25x faster                                                          |
| async_tree_memoization     | 578 ms                                                 | 465 ms: 1.24x faster                                                          |
| async_tree_cpu_io_mixed_tg | 726 ms                                                 | 604 ms: 1.20x faster                                                          |
| async_tree_cpu_io_mixed    | 726 ms                                                 | 607 ms: 1.20x faster                                                          |
| raytrace                   | 312 ms                                                 | 265 ms: 1.18x faster                                                          |
| deltablue                  | 3.72 ms                                                | 3.29 ms: 1.13x faster                                                         |
| logging_format             | 7.23 us                                                | 6.43 us: 1.13x faster                                                         |
| mypy2                      | 830 ms                                                 | 741 ms: 1.12x faster                                                          |
| logging_simple             | 6.46 us                                                | 5.78 us: 1.12x faster                                                         |
| pathlib                    | 19.3 ms                                                | 17.6 ms: 1.10x faster                                                         |
| tornado_http               | 103 ms                                                 | 94.1 ms: 1.09x faster                                                         |
| mako                       | 11.9 ms                                                | 11.0 ms: 1.09x faster                                                         |
| crypto_pyaes               | 81.9 ms                                                | 75.6 ms: 1.08x faster                                                         |
| regex_compile              | 148 ms                                                 | 137 ms: 1.08x faster                                                          |
| chaos                      | 67.0 ms                                                | 62.2 ms: 1.08x faster                                                         |
| nbody                      | 97.0 ms                                                | 90.3 ms: 1.07x faster                                                         |
| pickle_pure_python         | 324 us                                                 | 302 us: 1.07x faster                                                          |
| sympy_sum                  | 169 ms                                                 | 158 ms: 1.07x faster                                                          |
| scimark_monte_carlo        | 75.1 ms                                                | 70.3 ms: 1.07x faster                                                         |
| unpickle_list              | 5.29 us                                                | 4.98 us: 1.06x faster                                                         |
| float                      | 84.7 ms                                                | 79.8 ms: 1.06x faster                                                         |
| deepcopy_memo              | 40.7 us                                                | 38.5 us: 1.06x faster                                                         |
| sympy_str                  | 300 ms                                                 | 284 ms: 1.06x faster                                                          |
| sqlglot_transpile          | 1.68 ms                                                | 1.60 ms: 1.06x faster                                                         |
| sqlglot_parse              | 1.36 ms                                                | 1.29 ms: 1.05x faster                                                         |
| pickle_dict                | 35.5 us                                                | 33.9 us: 1.05x faster                                                         |
| chameleon                  | 7.41 ms                                                | 7.07 ms: 1.05x faster                                                         |
| tomli_loads                | 2.33 sec                                               | 2.22 sec: 1.05x faster                                                        |
| unpickle                   | 15.9 us                                                | 15.1 us: 1.05x faster                                                         |
| fannkuch                   | 417 ms                                                 | 399 ms: 1.05x faster                                                          |
| sympy_integrate            | 21.4 ms                                                | 20.6 ms: 1.04x faster                                                         |
| generators                 | 31.2 ms                                                | 30.1 ms: 1.04x faster                                                         |
| scimark_sor                | 129 ms                                                 | 125 ms: 1.04x faster                                                          |
| async_generators           | 463 ms                                                 | 448 ms: 1.03x faster                                                          |
| unpickle_pure_python       | 230 us                                                 | 223 us: 1.03x faster                                                          |
| dulwich_log                | 68.5 ms                                                | 66.3 ms: 1.03x faster                                                         |
| deepcopy                   | 371 us                                                 | 361 us: 1.03x faster                                                          |
| pyflate                    | 482 ms                                                 | 469 ms: 1.03x faster                                                          |
| pprint_safe_repr           | 776 ms                                                 | 755 ms: 1.03x faster                                                          |
| deepcopy_reduce            | 3.35 us                                                | 3.26 us: 1.03x faster                                                         |
| json_loads                 | 28.5 us                                                | 28.0 us: 1.02x faster                                                         |
| pprint_pformat             | 1.57 sec                                               | 1.54 sec: 1.02x faster                                                        |
| nqueens                    | 83.3 ms                                                | 82.4 ms: 1.01x faster                                                         |
| 2to3                       | 274 ms                                                 | 271 ms: 1.01x faster                                                          |
| pickle_list                | 5.08 us                                                | 5.03 us: 1.01x faster                                                         |
| gc_traversal               | 3.79 ms                                                | 3.76 ms: 1.01x faster                                                         |
| xml_etree_process          | 61.7 ms                                                | 61.2 ms: 1.01x faster                                                         |
| pickle                     | 11.6 us                                                | 11.5 us: 1.01x faster                                                         |
| bench_mp_pool              | 24.0 ms                                                | 23.8 ms: 1.01x faster                                                         |
| meteor_contest             | 112 ms                                                 | 112 ms: 1.01x faster                                                          |
| xml_etree_generate         | 89.2 ms                                                | 88.5 ms: 1.01x faster                                                         |
| scimark_fft                | 382 ms                                                 | 380 ms: 1.01x faster                                                          |
| bench_thread_pool          | 842 us                                                 | 838 us: 1.00x faster                                                          |
| xml_etree_iterparse        | 107 ms                                                 | 108 ms: 1.01x slower                                                          |
| regex_effbot               | 3.61 ms                                                | 3.65 ms: 1.01x slower                                                         |
| pidigits                   | 187 ms                                                 | 190 ms: 1.01x slower                                                          |
| mdp                        | 2.63 sec                                               | 2.67 sec: 1.01x slower                                                        |
| sqlglot_normalize          | 110 ms                                                 | 112 ms: 1.01x slower                                                          |
| aiohttp                    | 1.15 ms                                                | 1.17 ms: 1.02x slower                                                         |
| asyncio_websockets         | 551 ms                                                 | 563 ms: 1.02x slower                                                          |
| sqlglot_optimize           | 54.8 ms                                                | 56.0 ms: 1.02x slower                                                         |
| python_startup_no_site     | 6.94 ms                                                | 7.09 ms: 1.02x slower                                                         |
| json_dumps                 | 10.4 ms                                                | 10.6 ms: 1.02x slower                                                         |
| gunicorn                   | 1.24 ms                                                | 1.27 ms: 1.02x slower                                                         |
| docutils                   | 2.77 sec                                               | 2.84 sec: 1.03x slower                                                        |
| scimark_lu                 | 118 ms                                                 | 121 ms: 1.03x slower                                                          |
| django_template            | 34.6 ms                                                | 35.6 ms: 1.03x slower                                                         |
| asyncio_tcp                | 491 ms                                                 | 505 ms: 1.03x slower                                                          |
| asyncio_tcp_ssl            | 1.79 sec                                               | 1.84 sec: 1.03x slower                                                        |
| go                         | 139 ms                                                 | 144 ms: 1.03x slower                                                          |
| richards_super             | 51.5 ms                                                | 54.0 ms: 1.05x slower                                                         |
| sqlite_synth               | 2.83 us                                                | 2.97 us: 1.05x slower                                                         |
| richards                   | 45.8 ms                                                | 48.2 ms: 1.05x slower                                                         |
| regex_dna                  | 212 ms                                                 | 226 ms: 1.06x slower                                                          |
| regex_v8                   | 23.1 ms                                                | 24.8 ms: 1.07x slower                                                         |
| scimark_sparse_mat_mult    | 5.06 ms                                                | 5.46 ms: 1.08x slower                                                         |
| python_startup             | 9.55 ms                                                | 10.5 ms: 1.10x slower                                                         |
| create_gc_cycles           | 1.48 ms                                                | 1.73 ms: 1.17x slower                                                         |
| telco                      | 7.10 ms                                                | 8.85 ms: 1.25x slower                                                         |
| coverage                   | 72.7 ms                                                | 97.6 ms: 1.34x slower                                                         |
| Geometric mean             | (ref)                                                  | 1.04x faster                                                                  |

Benchmark hidden because not significant (9): dask, json, pycparser, logging_silent, hexiom, coroutines, xml_etree_parse, sympy_expand, spectral_norm
Ignored benchmarks (3) of results/bm-20231002-3.12.0-0fb18b0/bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0.json: sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
Ignored benchmarks (6) of results/bm-20240416-3.13.0a6+-83ebcf5/bm-20240416-linux-x86_64-faster%2dcpython-faster_alloc_free-3.13.0a6+-83ebcf5.json: djangocms, genshi_text, genshi_xml, html5lib, pylint, thrift

# HPT report

- Reliability score: 99.43% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 0.96x