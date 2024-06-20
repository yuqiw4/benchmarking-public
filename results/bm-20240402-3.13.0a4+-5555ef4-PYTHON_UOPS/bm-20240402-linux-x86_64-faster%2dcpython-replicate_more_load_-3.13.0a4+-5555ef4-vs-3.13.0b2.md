# Results vs. 3.13.0b2

- fork: faster-cpython
- ref: replicate_more_load_
- machine: linux-x86_64
- commit hash: 5555ef4
- commit date: 2024-04-02
- overall geometric mean: 1.10x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.06x slower
- Memory change: 0.97x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240402-linux-x86_64-faster%2dcpython-replicate_more_load_-3.13.0a4+-5555ef4 |
|----------------|:----------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| 2to3           | 274 ms                                                     | 300 ms: 1.10x slower                                                             |
| chameleon      | 7.22 ms                                                    | 7.08 ms: 1.02x faster                                                            |
| docutils       | 2.83 sec                                                   | 2.87 sec: 1.02x slower                                                           |
| html5lib       | 67.2 ms                                                    | 71.1 ms: 1.06x slower                                                            |
| tornado_http   | 94.6 ms                                                    | 103 ms: 1.09x slower                                                             |
| Geometric mean | (ref)                                                      | 1.05x slower                                                                     |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240402-linux-x86_64-faster%2dcpython-replicate_more_load_-3.13.0a4+-5555ef4 |
|----------------------------|:----------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| async_tree_cpu_io_mixed    | 611 ms                                                     | 747 ms: 1.22x slower                                                             |
| async_tree_none            | 378 ms                                                     | 463 ms: 1.22x slower                                                             |
| async_tree_memoization     | 463 ms                                                     | 594 ms: 1.28x slower                                                             |
| async_tree_cpu_io_mixed_tg | 587 ms                                                     | 754 ms: 1.28x slower                                                             |
| async_tree_io              | 939 ms                                                     | 1.24 sec: 1.32x slower                                                           |
| async_tree_io_tg           | 936 ms                                                     | 1.26 sec: 1.35x slower                                                           |
| async_tree_memoization_tg  | 444 ms                                                     | 603 ms: 1.36x slower                                                             |
| async_tree_none_tg         | 336 ms                                                     | 471 ms: 1.40x slower                                                             |
| Geometric mean             | (ref)                                                      | 1.30x slower                                                                     |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240402-linux-x86_64-faster%2dcpython-replicate_more_load_-3.13.0a4+-5555ef4 |
|----------------|:----------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| pidigits       | 191 ms                                                     | 191 ms: 1.00x faster                                                             |
| float          | 78.9 ms                                                    | 94.7 ms: 1.20x slower                                                            |
| nbody          | 88.3 ms                                                    | 123 ms: 1.40x slower                                                             |
| Geometric mean | (ref)                                                      | 1.19x slower                                                                     |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240402-linux-x86_64-faster%2dcpython-replicate_more_load_-3.13.0a4+-5555ef4 |
|----------------|:----------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| regex_dna      | 221 ms                                                     | 213 ms: 1.04x faster                                                             |
| regex_effbot   | 3.67 ms                                                    | 3.55 ms: 1.03x faster                                                            |
| regex_compile  | 137 ms                                                     | 178 ms: 1.30x slower                                                             |
| Geometric mean | (ref)                                                      | 1.05x slower                                                                     |

Benchmark hidden because not significant (1): regex_v8

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240402-linux-x86_64-faster%2dcpython-replicate_more_load_-3.13.0a4+-5555ef4 |
|----------------------|:----------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| unpickle_list        | 5.34 us                                                    | 5.12 us: 1.04x faster                                                            |
| json_loads           | 28.9 us                                                    | 28.4 us: 1.02x faster                                                            |
| pickle_dict          | 34.8 us                                                    | 34.9 us: 1.00x slower                                                            |
| unpickle             | 15.1 us                                                    | 15.4 us: 1.02x slower                                                            |
| xml_etree_process    | 61.2 ms                                                    | 62.8 ms: 1.03x slower                                                            |
| pickle_list          | 5.11 us                                                    | 5.25 us: 1.03x slower                                                            |
| pickle_pure_python   | 305 us                                                     | 314 us: 1.03x slower                                                             |
| pickle               | 11.5 us                                                    | 12.0 us: 1.04x slower                                                            |
| xml_etree_generate   | 87.4 ms                                                    | 91.6 ms: 1.05x slower                                                            |
| xml_etree_iterparse  | 107 ms                                                     | 113 ms: 1.05x slower                                                             |
| tomli_loads          | 2.12 sec                                                   | 2.53 sec: 1.19x slower                                                           |
| unpickle_pure_python | 218 us                                                     | 278 us: 1.28x slower                                                             |
| Geometric mean       | (ref)                                                      | 1.04x slower                                                                     |

Benchmark hidden because not significant (2): json_dumps, xml_etree_parse

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240402-linux-x86_64-faster%2dcpython-replicate_more_load_-3.13.0a4+-5555ef4 |
|------------------------|:----------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| python_startup         | 10.8 ms                                                    | 10.5 ms: 1.02x faster                                                            |
| python_startup_no_site | 7.11 ms                                                    | 9.07 ms: 1.28x slower                                                            |
| Geometric mean         | (ref)                                                      | 1.12x slower                                                                     |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240402-linux-x86_64-faster%2dcpython-replicate_more_load_-3.13.0a4+-5555ef4 |
|-----------------|:----------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| django_template | 34.8 ms                                                    | 34.5 ms: 1.01x faster                                                            |
| mako            | 11.2 ms                                                    | 12.9 ms: 1.15x slower                                                            |
| genshi_text     | 23.7 ms                                                    | 28.0 ms: 1.18x slower                                                            |
| genshi_xml      | 51.6 ms                                                    | 64.9 ms: 1.26x slower                                                            |
| Geometric mean  | (ref)                                                      | 1.14x slower                                                                     |

All benchmarks:
===============

| Benchmark                  | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240402-linux-x86_64-faster%2dcpython-replicate_more_load_-3.13.0a4+-5555ef4 |
|----------------------------|:----------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| typing_runtime_protocols   | 165 us                                                     | 118 us: 1.39x faster                                                             |
| create_gc_cycles           | 1.82 ms                                                    | 1.55 ms: 1.17x faster                                                            |
| deepcopy_reduce            | 3.35 us                                                    | 3.11 us: 1.08x faster                                                            |
| unpickle_list              | 5.34 us                                                    | 5.12 us: 1.04x faster                                                            |
| regex_dna                  | 221 ms                                                     | 213 ms: 1.04x faster                                                             |
| regex_effbot               | 3.67 ms                                                    | 3.55 ms: 1.03x faster                                                            |
| gc_traversal               | 3.98 ms                                                    | 3.85 ms: 1.03x faster                                                            |
| python_startup             | 10.8 ms                                                    | 10.5 ms: 1.02x faster                                                            |
| chameleon                  | 7.22 ms                                                    | 7.08 ms: 1.02x faster                                                            |
| json_loads                 | 28.9 us                                                    | 28.4 us: 1.02x faster                                                            |
| mdp                        | 2.79 sec                                                   | 2.75 sec: 1.01x faster                                                           |
| sqlite_synth               | 2.99 us                                                    | 2.95 us: 1.01x faster                                                            |
| django_template            | 34.8 ms                                                    | 34.5 ms: 1.01x faster                                                            |
| logging_silent             | 105 ns                                                     | 104 ns: 1.01x faster                                                             |
| asyncio_websockets         | 567 ms                                                     | 564 ms: 1.01x faster                                                             |
| pidigits                   | 191 ms                                                     | 191 ms: 1.00x faster                                                             |
| pickle_dict                | 34.8 us                                                    | 34.9 us: 1.00x slower                                                            |
| asyncio_tcp_ssl            | 1.84 sec                                                   | 1.86 sec: 1.01x slower                                                           |
| thrift                     | 823 us                                                     | 834 us: 1.01x slower                                                             |
| docutils                   | 2.83 sec                                                   | 2.87 sec: 1.02x slower                                                           |
| unpickle                   | 15.1 us                                                    | 15.4 us: 1.02x slower                                                            |
| generators                 | 29.6 ms                                                    | 30.4 ms: 1.03x slower                                                            |
| gunicorn                   | 1.28 ms                                                    | 1.31 ms: 1.03x slower                                                            |
| xml_etree_process          | 61.2 ms                                                    | 62.8 ms: 1.03x slower                                                            |
| dask                       | 369 ms                                                     | 379 ms: 1.03x slower                                                             |
| sqlglot_normalize          | 110 ms                                                     | 113 ms: 1.03x slower                                                             |
| pickle_list                | 5.11 us                                                    | 5.25 us: 1.03x slower                                                            |
| pickle_pure_python         | 305 us                                                     | 314 us: 1.03x slower                                                             |
| djangocms                  | 31.5 us                                                    | 32.4 us: 1.03x slower                                                            |
| aiohttp                    | 1.18 ms                                                    | 1.22 ms: 1.03x slower                                                            |
| coroutines                 | 23.2 ms                                                    | 24.0 ms: 1.04x slower                                                            |
| pickle                     | 11.5 us                                                    | 12.0 us: 1.04x slower                                                            |
| xml_etree_generate         | 87.4 ms                                                    | 91.6 ms: 1.05x slower                                                            |
| bench_thread_pool          | 834 us                                                     | 873 us: 1.05x slower                                                             |
| xml_etree_iterparse        | 107 ms                                                     | 113 ms: 1.05x slower                                                             |
| sympy_integrate            | 20.5 ms                                                    | 21.5 ms: 1.05x slower                                                            |
| coverage                   | 93.1 ms                                                    | 97.8 ms: 1.05x slower                                                            |
| telco                      | 8.41 ms                                                    | 8.85 ms: 1.05x slower                                                            |
| html5lib                   | 67.2 ms                                                    | 71.1 ms: 1.06x slower                                                            |
| deepcopy_memo              | 39.7 us                                                    | 42.2 us: 1.06x slower                                                            |
| sympy_sum                  | 156 ms                                                     | 166 ms: 1.07x slower                                                             |
| meteor_contest             | 110 ms                                                     | 117 ms: 1.07x slower                                                             |
| sympy_str                  | 282 ms                                                     | 306 ms: 1.08x slower                                                             |
| async_generators           | 442 ms                                                     | 480 ms: 1.09x slower                                                             |
| sympy_expand               | 473 ms                                                     | 514 ms: 1.09x slower                                                             |
| tornado_http               | 94.6 ms                                                    | 103 ms: 1.09x slower                                                             |
| 2to3                       | 274 ms                                                     | 300 ms: 1.10x slower                                                             |
| dulwich_log                | 67.2 ms                                                    | 73.7 ms: 1.10x slower                                                            |
| richards_super             | 57.4 ms                                                    | 63.0 ms: 1.10x slower                                                            |
| crypto_pyaes               | 77.5 ms                                                    | 85.4 ms: 1.10x slower                                                            |
| sqlglot_optimize           | 55.5 ms                                                    | 61.2 ms: 1.10x slower                                                            |
| richards                   | 50.9 ms                                                    | 56.3 ms: 1.11x slower                                                            |
| sqlglot_transpile          | 1.63 ms                                                    | 1.81 ms: 1.11x slower                                                            |
| logging_simple             | 5.74 us                                                    | 6.37 us: 1.11x slower                                                            |
| sqlglot_parse              | 1.32 ms                                                    | 1.47 ms: 1.11x slower                                                            |
| logging_format             | 6.47 us                                                    | 7.19 us: 1.11x slower                                                            |
| pathlib                    | 17.3 ms                                                    | 19.3 ms: 1.11x slower                                                            |
| pprint_safe_repr           | 758 ms                                                     | 866 ms: 1.14x slower                                                             |
| mako                       | 11.2 ms                                                    | 12.9 ms: 1.15x slower                                                            |
| scimark_fft                | 392 ms                                                     | 450 ms: 1.15x slower                                                             |
| pycparser                  | 1.16 sec                                                   | 1.33 sec: 1.15x slower                                                           |
| pprint_pformat             | 1.56 sec                                                   | 1.82 sec: 1.17x slower                                                           |
| scimark_sparse_mat_mult    | 5.27 ms                                                    | 6.20 ms: 1.18x slower                                                            |
| genshi_text                | 23.7 ms                                                    | 28.0 ms: 1.18x slower                                                            |
| tomli_loads                | 2.12 sec                                                   | 2.53 sec: 1.19x slower                                                           |
| deltablue                  | 3.25 ms                                                    | 3.88 ms: 1.19x slower                                                            |
| fannkuch                   | 402 ms                                                     | 480 ms: 1.19x slower                                                             |
| float                      | 78.9 ms                                                    | 94.7 ms: 1.20x slower                                                            |
| spectral_norm              | 116 ms                                                     | 140 ms: 1.20x slower                                                             |
| scimark_sor                | 127 ms                                                     | 154 ms: 1.21x slower                                                             |
| async_tree_cpu_io_mixed    | 611 ms                                                     | 747 ms: 1.22x slower                                                             |
| async_tree_none            | 378 ms                                                     | 463 ms: 1.22x slower                                                             |
| pyflate                    | 484 ms                                                     | 593 ms: 1.22x slower                                                             |
| chaos                      | 61.3 ms                                                    | 75.2 ms: 1.23x slower                                                            |
| go                         | 145 ms                                                     | 179 ms: 1.23x slower                                                             |
| mypy2                      | 742 ms                                                     | 918 ms: 1.24x slower                                                             |
| scimark_monte_carlo        | 69.2 ms                                                    | 85.9 ms: 1.24x slower                                                            |
| nqueens                    | 81.4 ms                                                    | 101 ms: 1.24x slower                                                             |
| genshi_xml                 | 51.6 ms                                                    | 64.9 ms: 1.26x slower                                                            |
| comprehensions             | 16.6 us                                                    | 20.9 us: 1.26x slower                                                            |
| python_startup_no_site     | 7.11 ms                                                    | 9.07 ms: 1.28x slower                                                            |
| unpickle_pure_python       | 218 us                                                     | 278 us: 1.28x slower                                                             |
| async_tree_memoization     | 463 ms                                                     | 594 ms: 1.28x slower                                                             |
| async_tree_cpu_io_mixed_tg | 587 ms                                                     | 754 ms: 1.28x slower                                                             |
| raytrace                   | 267 ms                                                     | 346 ms: 1.30x slower                                                             |
| regex_compile              | 137 ms                                                     | 178 ms: 1.30x slower                                                             |
| scimark_lu                 | 122 ms                                                     | 160 ms: 1.32x slower                                                             |
| async_tree_io              | 939 ms                                                     | 1.24 sec: 1.32x slower                                                           |
| async_tree_io_tg           | 936 ms                                                     | 1.26 sec: 1.35x slower                                                           |
| async_tree_memoization_tg  | 444 ms                                                     | 603 ms: 1.36x slower                                                             |
| nbody                      | 88.3 ms                                                    | 123 ms: 1.40x slower                                                             |
| async_tree_none_tg         | 336 ms                                                     | 471 ms: 1.40x slower                                                             |
| hexiom                     | 6.30 ms                                                    | 9.07 ms: 1.44x slower                                                            |
| Geometric mean             | (ref)                                                      | 1.10x slower                                                                     |

Benchmark hidden because not significant (8): json_dumps, xml_etree_parse, deepcopy, regex_v8, bench_mp_pool, asyncio_tcp, json, pylint
Ignored benchmarks (2) of results/bm-20240605-3.13.0b2-3a83b17/bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17.json: bpe_tokeniser, flaskblogging
Ignored benchmarks (1) of results/bm-20240402-3.13.0a4+-5555ef4-PYTHON_UOPS/bm-20240402-linux-x86_64-faster%2dcpython-replicate_more_load_-3.13.0a4+-5555ef4.json: unpack_sequence

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.08x
- 95% likely to have a slowdown of 1.07x
- 99% likely to have a slowdown of 1.06x

# Memory
- memory change: 0.97x