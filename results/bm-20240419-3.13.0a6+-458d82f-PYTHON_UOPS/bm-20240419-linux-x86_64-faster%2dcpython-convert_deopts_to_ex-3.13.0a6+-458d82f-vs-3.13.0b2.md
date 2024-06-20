# Results vs. 3.13.0b2

- fork: faster-cpython
- ref: convert_deopts_to_ex
- machine: linux-x86_64
- commit hash: 458d82f
- commit date: 2024-04-19
- overall geometric mean: 1.10x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.06x slower
- Memory change: 0.99x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240419-linux-x86_64-faster%2dcpython-convert_deopts_to_ex-3.13.0a6+-458d82f |
|----------------|:----------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| 2to3           | 274 ms                                                     | 305 ms: 1.11x slower                                                             |
| chameleon      | 7.22 ms                                                    | 7.61 ms: 1.05x slower                                                            |
| docutils       | 2.83 sec                                                   | 3.14 sec: 1.11x slower                                                           |
| html5lib       | 67.2 ms                                                    | 72.2 ms: 1.07x slower                                                            |
| tornado_http   | 94.6 ms                                                    | 102 ms: 1.08x slower                                                             |
| Geometric mean | (ref)                                                      | 1.09x slower                                                                     |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240419-linux-x86_64-faster%2dcpython-convert_deopts_to_ex-3.13.0a6+-458d82f |
|----------------------------|:----------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| async_tree_io_tg           | 936 ms                                                     | 966 ms: 1.03x slower                                                             |
| async_tree_cpu_io_mixed    | 611 ms                                                     | 635 ms: 1.04x slower                                                             |
| async_tree_io              | 939 ms                                                     | 976 ms: 1.04x slower                                                             |
| async_tree_memoization_tg  | 444 ms                                                     | 467 ms: 1.05x slower                                                             |
| async_tree_none_tg         | 336 ms                                                     | 357 ms: 1.06x slower                                                             |
| async_tree_cpu_io_mixed_tg | 587 ms                                                     | 629 ms: 1.07x slower                                                             |
| async_tree_memoization     | 463 ms                                                     | 503 ms: 1.09x slower                                                             |
| Geometric mean             | (ref)                                                      | 1.05x slower                                                                     |

Benchmark hidden because not significant (1): async_tree_none

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240419-linux-x86_64-faster%2dcpython-convert_deopts_to_ex-3.13.0a6+-458d82f |
|----------------|:----------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| pidigits       | 191 ms                                                     | 192 ms: 1.00x slower                                                             |
| float          | 78.9 ms                                                    | 89.2 ms: 1.13x slower                                                            |
| nbody          | 88.3 ms                                                    | 122 ms: 1.38x slower                                                             |
| Geometric mean | (ref)                                                      | 1.16x slower                                                                     |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240419-linux-x86_64-faster%2dcpython-convert_deopts_to_ex-3.13.0a6+-458d82f |
|----------------|:----------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| regex_dna      | 221 ms                                                     | 224 ms: 1.01x slower                                                             |
| regex_effbot   | 3.67 ms                                                    | 3.73 ms: 1.02x slower                                                            |
| regex_compile  | 137 ms                                                     | 181 ms: 1.32x slower                                                             |
| Geometric mean | (ref)                                                      | 1.08x slower                                                                     |

Benchmark hidden because not significant (1): regex_v8

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240419-linux-x86_64-faster%2dcpython-convert_deopts_to_ex-3.13.0a6+-458d82f |
|----------------------|:----------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| xml_etree_parse      | 162 ms                                                     | 152 ms: 1.07x faster                                                             |
| pickle_dict          | 34.8 us                                                    | 32.8 us: 1.06x faster                                                            |
| pickle_list          | 5.11 us                                                    | 4.83 us: 1.06x faster                                                            |
| json_loads           | 28.9 us                                                    | 27.8 us: 1.04x faster                                                            |
| unpickle             | 15.1 us                                                    | 15.6 us: 1.03x slower                                                            |
| xml_etree_iterparse  | 107 ms                                                     | 111 ms: 1.03x slower                                                             |
| pickle_pure_python   | 305 us                                                     | 316 us: 1.04x slower                                                             |
| pickle               | 11.5 us                                                    | 12.1 us: 1.05x slower                                                            |
| xml_etree_process    | 61.2 ms                                                    | 65.1 ms: 1.06x slower                                                            |
| xml_etree_generate   | 87.4 ms                                                    | 93.5 ms: 1.07x slower                                                            |
| tomli_loads          | 2.12 sec                                                   | 2.55 sec: 1.20x slower                                                           |
| unpickle_pure_python | 218 us                                                     | 282 us: 1.29x slower                                                             |
| Geometric mean       | (ref)                                                      | 1.04x slower                                                                     |

Benchmark hidden because not significant (2): unpickle_list, json_dumps

Benchmarks with tag 'startup':
==============================

| Benchmark      | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240419-linux-x86_64-faster%2dcpython-convert_deopts_to_ex-3.13.0a6+-458d82f |
|----------------|:----------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| python_startup | 10.8 ms                                                    | 10.5 ms: 1.02x faster                                                            |
| Geometric mean | (ref)                                                      | 1.01x faster                                                                     |

Benchmark hidden because not significant (1): python_startup_no_site

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240419-linux-x86_64-faster%2dcpython-convert_deopts_to_ex-3.13.0a6+-458d82f |
|-----------------|:----------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| django_template | 34.8 ms                                                    | 41.3 ms: 1.19x slower                                                            |
| mako            | 11.2 ms                                                    | 13.6 ms: 1.21x slower                                                            |
| genshi_text     | 23.7 ms                                                    | 28.7 ms: 1.21x slower                                                            |
| genshi_xml      | 51.6 ms                                                    | 64.7 ms: 1.25x slower                                                            |
| Geometric mean  | (ref)                                                      | 1.22x slower                                                                     |

All benchmarks:
===============

| Benchmark                  | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240419-linux-x86_64-faster%2dcpython-convert_deopts_to_ex-3.13.0a6+-458d82f |
|----------------------------|:----------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| typing_runtime_protocols   | 165 us                                                     | 124 us: 1.33x faster                                                             |
| xml_etree_parse            | 162 ms                                                     | 152 ms: 1.07x faster                                                             |
| pickle_dict                | 34.8 us                                                    | 32.8 us: 1.06x faster                                                            |
| pickle_list                | 5.11 us                                                    | 4.83 us: 1.06x faster                                                            |
| gc_traversal               | 3.98 ms                                                    | 3.80 ms: 1.05x faster                                                            |
| json_loads                 | 28.9 us                                                    | 27.8 us: 1.04x faster                                                            |
| json                       | 5.31 ms                                                    | 5.14 ms: 1.03x faster                                                            |
| create_gc_cycles           | 1.82 ms                                                    | 1.76 ms: 1.03x faster                                                            |
| python_startup             | 10.8 ms                                                    | 10.5 ms: 1.02x faster                                                            |
| pidigits                   | 191 ms                                                     | 192 ms: 1.00x slower                                                             |
| generators                 | 29.6 ms                                                    | 29.8 ms: 1.01x slower                                                            |
| sqlite_synth               | 2.99 us                                                    | 3.01 us: 1.01x slower                                                            |
| asyncio_tcp_ssl            | 1.84 sec                                                   | 1.86 sec: 1.01x slower                                                           |
| logging_silent             | 105 ns                                                     | 106 ns: 1.01x slower                                                             |
| regex_dna                  | 221 ms                                                     | 224 ms: 1.01x slower                                                             |
| regex_effbot               | 3.67 ms                                                    | 3.73 ms: 1.02x slower                                                            |
| mdp                        | 2.79 sec                                                   | 2.84 sec: 1.02x slower                                                           |
| thrift                     | 823 us                                                     | 847 us: 1.03x slower                                                             |
| async_tree_io_tg           | 936 ms                                                     | 966 ms: 1.03x slower                                                             |
| unpickle                   | 15.1 us                                                    | 15.6 us: 1.03x slower                                                            |
| xml_etree_iterparse        | 107 ms                                                     | 111 ms: 1.03x slower                                                             |
| pickle_pure_python         | 305 us                                                     | 316 us: 1.04x slower                                                             |
| async_tree_cpu_io_mixed    | 611 ms                                                     | 635 ms: 1.04x slower                                                             |
| async_tree_io              | 939 ms                                                     | 976 ms: 1.04x slower                                                             |
| gunicorn                   | 1.28 ms                                                    | 1.33 ms: 1.04x slower                                                            |
| deepcopy                   | 367 us                                                     | 384 us: 1.05x slower                                                             |
| coroutines                 | 23.2 ms                                                    | 24.3 ms: 1.05x slower                                                            |
| asyncio_tcp                | 508 ms                                                     | 533 ms: 1.05x slower                                                             |
| coverage                   | 93.1 ms                                                    | 97.9 ms: 1.05x slower                                                            |
| dask                       | 369 ms                                                     | 389 ms: 1.05x slower                                                             |
| async_tree_memoization_tg  | 444 ms                                                     | 467 ms: 1.05x slower                                                             |
| pickle                     | 11.5 us                                                    | 12.1 us: 1.05x slower                                                            |
| aiohttp                    | 1.18 ms                                                    | 1.24 ms: 1.05x slower                                                            |
| chameleon                  | 7.22 ms                                                    | 7.61 ms: 1.05x slower                                                            |
| async_generators           | 442 ms                                                     | 468 ms: 1.06x slower                                                             |
| djangocms                  | 31.5 us                                                    | 33.4 us: 1.06x slower                                                            |
| async_tree_none_tg         | 336 ms                                                     | 357 ms: 1.06x slower                                                             |
| bench_thread_pool          | 834 us                                                     | 886 us: 1.06x slower                                                             |
| xml_etree_process          | 61.2 ms                                                    | 65.1 ms: 1.06x slower                                                            |
| xml_etree_generate         | 87.4 ms                                                    | 93.5 ms: 1.07x slower                                                            |
| async_tree_cpu_io_mixed_tg | 587 ms                                                     | 629 ms: 1.07x slower                                                             |
| html5lib                   | 67.2 ms                                                    | 72.2 ms: 1.07x slower                                                            |
| pathlib                    | 17.3 ms                                                    | 18.7 ms: 1.08x slower                                                            |
| deepcopy_memo              | 39.7 us                                                    | 42.9 us: 1.08x slower                                                            |
| telco                      | 8.41 ms                                                    | 9.11 ms: 1.08x slower                                                            |
| tornado_http               | 94.6 ms                                                    | 102 ms: 1.08x slower                                                             |
| async_tree_memoization     | 463 ms                                                     | 503 ms: 1.09x slower                                                             |
| richards_super             | 57.4 ms                                                    | 62.9 ms: 1.10x slower                                                            |
| pycparser                  | 1.16 sec                                                   | 1.27 sec: 1.10x slower                                                           |
| pylint                     | 317 ms                                                     | 350 ms: 1.10x slower                                                             |
| richards                   | 50.9 ms                                                    | 56.3 ms: 1.11x slower                                                            |
| sqlglot_transpile          | 1.63 ms                                                    | 1.81 ms: 1.11x slower                                                            |
| docutils                   | 2.83 sec                                                   | 3.14 sec: 1.11x slower                                                           |
| 2to3                       | 274 ms                                                     | 305 ms: 1.11x slower                                                             |
| mypy2                      | 742 ms                                                     | 829 ms: 1.12x slower                                                             |
| dulwich_log                | 67.2 ms                                                    | 75.1 ms: 1.12x slower                                                            |
| sqlglot_parse              | 1.32 ms                                                    | 1.48 ms: 1.12x slower                                                            |
| float                      | 78.9 ms                                                    | 89.2 ms: 1.13x slower                                                            |
| meteor_contest             | 110 ms                                                     | 125 ms: 1.14x slower                                                             |
| sqlglot_normalize          | 110 ms                                                     | 126 ms: 1.14x slower                                                             |
| sympy_sum                  | 156 ms                                                     | 178 ms: 1.14x slower                                                             |
| sympy_integrate            | 20.5 ms                                                    | 23.5 ms: 1.15x slower                                                            |
| sympy_expand               | 473 ms                                                     | 544 ms: 1.15x slower                                                             |
| sympy_str                  | 282 ms                                                     | 325 ms: 1.15x slower                                                             |
| sqlglot_optimize           | 55.5 ms                                                    | 64.2 ms: 1.16x slower                                                            |
| scimark_fft                | 392 ms                                                     | 457 ms: 1.16x slower                                                             |
| logging_format             | 6.47 us                                                    | 7.54 us: 1.17x slower                                                            |
| scimark_sparse_mat_mult    | 5.27 ms                                                    | 6.20 ms: 1.18x slower                                                            |
| logging_simple             | 5.74 us                                                    | 6.76 us: 1.18x slower                                                            |
| django_template            | 34.8 ms                                                    | 41.3 ms: 1.19x slower                                                            |
| tomli_loads                | 2.12 sec                                                   | 2.55 sec: 1.20x slower                                                           |
| mako                       | 11.2 ms                                                    | 13.6 ms: 1.21x slower                                                            |
| genshi_text                | 23.7 ms                                                    | 28.7 ms: 1.21x slower                                                            |
| crypto_pyaes               | 77.5 ms                                                    | 94.1 ms: 1.21x slower                                                            |
| raytrace                   | 267 ms                                                     | 326 ms: 1.22x slower                                                             |
| spectral_norm              | 116 ms                                                     | 144 ms: 1.24x slower                                                             |
| pyflate                    | 484 ms                                                     | 600 ms: 1.24x slower                                                             |
| fannkuch                   | 402 ms                                                     | 501 ms: 1.25x slower                                                             |
| scimark_sor                | 127 ms                                                     | 159 ms: 1.25x slower                                                             |
| genshi_xml                 | 51.6 ms                                                    | 64.7 ms: 1.25x slower                                                            |
| scimark_monte_carlo        | 69.2 ms                                                    | 88.3 ms: 1.28x slower                                                            |
| pprint_safe_repr           | 758 ms                                                     | 974 ms: 1.28x slower                                                             |
| unpickle_pure_python       | 218 us                                                     | 282 us: 1.29x slower                                                             |
| pprint_pformat             | 1.56 sec                                                   | 2.02 sec: 1.30x slower                                                           |
| chaos                      | 61.3 ms                                                    | 80.9 ms: 1.32x slower                                                            |
| go                         | 145 ms                                                     | 191 ms: 1.32x slower                                                             |
| regex_compile              | 137 ms                                                     | 181 ms: 1.32x slower                                                             |
| nqueens                    | 81.4 ms                                                    | 109 ms: 1.33x slower                                                             |
| deltablue                  | 3.25 ms                                                    | 4.37 ms: 1.34x slower                                                            |
| nbody                      | 88.3 ms                                                    | 122 ms: 1.38x slower                                                             |
| scimark_lu                 | 122 ms                                                     | 173 ms: 1.42x slower                                                             |
| comprehensions             | 16.6 us                                                    | 23.9 us: 1.44x slower                                                            |
| hexiom                     | 6.30 ms                                                    | 9.65 ms: 1.53x slower                                                            |
| Geometric mean             | (ref)                                                      | 1.10x slower                                                                     |

Benchmark hidden because not significant (8): async_tree_none, deepcopy_reduce, unpickle_list, json_dumps, python_startup_no_site, asyncio_websockets, bench_mp_pool, regex_v8
Ignored benchmarks (2) of results/bm-20240605-3.13.0b2-3a83b17/bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17.json: bpe_tokeniser, flaskblogging

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.08x
- 95% likely to have a slowdown of 1.07x
- 99% likely to have a slowdown of 1.06x

# Memory
- memory change: 0.99x