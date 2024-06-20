# Results vs. 3.13.0b2

- fork: faster-cpython
- ref: move_set_ip_to_exits
- machine: linux-x86_64
- commit hash: ed60e2e
- commit date: 2024-04-19
- overall geometric mean: 1.12x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.08x slower
- Memory change: 0.99x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240419-linux-x86_64-faster%2dcpython-move_set_ip_to_exits-3.13.0a6+-ed60e2e |
|----------------|:----------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| 2to3           | 274 ms                                                     | 311 ms: 1.13x slower                                                             |
| chameleon      | 7.22 ms                                                    | 8.08 ms: 1.12x slower                                                            |
| docutils       | 2.83 sec                                                   | 3.15 sec: 1.11x slower                                                           |
| html5lib       | 67.2 ms                                                    | 72.9 ms: 1.08x slower                                                            |
| tornado_http   | 94.6 ms                                                    | 104 ms: 1.10x slower                                                             |
| Geometric mean | (ref)                                                      | 1.11x slower                                                                     |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240419-linux-x86_64-faster%2dcpython-move_set_ip_to_exits-3.13.0a6+-ed60e2e |
|----------------------------|:----------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| async_tree_io              | 939 ms                                                     | 968 ms: 1.03x slower                                                             |
| async_tree_cpu_io_mixed    | 611 ms                                                     | 646 ms: 1.06x slower                                                             |
| async_tree_io_tg           | 936 ms                                                     | 1000 ms: 1.07x slower                                                            |
| async_tree_memoization_tg  | 444 ms                                                     | 476 ms: 1.07x slower                                                             |
| async_tree_cpu_io_mixed_tg | 587 ms                                                     | 640 ms: 1.09x slower                                                             |
| async_tree_none_tg         | 336 ms                                                     | 367 ms: 1.09x slower                                                             |
| async_tree_memoization     | 463 ms                                                     | 511 ms: 1.10x slower                                                             |
| Geometric mean             | (ref)                                                      | 1.06x slower                                                                     |

Benchmark hidden because not significant (1): async_tree_none

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240419-linux-x86_64-faster%2dcpython-move_set_ip_to_exits-3.13.0a6+-ed60e2e |
|----------------|:----------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| pidigits       | 191 ms                                                     | 200 ms: 1.05x slower                                                             |
| float          | 78.9 ms                                                    | 93.3 ms: 1.18x slower                                                            |
| nbody          | 88.3 ms                                                    | 127 ms: 1.44x slower                                                             |
| Geometric mean | (ref)                                                      | 1.21x slower                                                                     |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240419-linux-x86_64-faster%2dcpython-move_set_ip_to_exits-3.13.0a6+-ed60e2e |
|----------------|:----------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| regex_effbot   | 3.67 ms                                                    | 3.68 ms: 1.00x slower                                                            |
| regex_dna      | 221 ms                                                     | 227 ms: 1.03x slower                                                             |
| regex_v8       | 25.1 ms                                                    | 26.0 ms: 1.03x slower                                                            |
| regex_compile  | 137 ms                                                     | 191 ms: 1.40x slower                                                             |
| Geometric mean | (ref)                                                      | 1.10x slower                                                                     |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240419-linux-x86_64-faster%2dcpython-move_set_ip_to_exits-3.13.0a6+-ed60e2e |
|----------------------|:----------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| xml_etree_parse      | 162 ms                                                     | 152 ms: 1.06x faster                                                             |
| json_loads           | 28.9 us                                                    | 27.7 us: 1.04x faster                                                            |
| json_dumps           | 10.7 ms                                                    | 10.7 ms: 1.01x faster                                                            |
| unpickle             | 15.1 us                                                    | 15.1 us: 1.00x faster                                                            |
| pickle_dict          | 34.8 us                                                    | 35.2 us: 1.01x slower                                                            |
| pickle               | 11.5 us                                                    | 11.6 us: 1.01x slower                                                            |
| pickle_pure_python   | 305 us                                                     | 310 us: 1.01x slower                                                             |
| unpickle_list        | 5.34 us                                                    | 5.46 us: 1.02x slower                                                            |
| xml_etree_iterparse  | 107 ms                                                     | 110 ms: 1.03x slower                                                             |
| xml_etree_process    | 61.2 ms                                                    | 65.0 ms: 1.06x slower                                                            |
| xml_etree_generate   | 87.4 ms                                                    | 96.0 ms: 1.10x slower                                                            |
| tomli_loads          | 2.12 sec                                                   | 2.69 sec: 1.27x slower                                                           |
| unpickle_pure_python | 218 us                                                     | 303 us: 1.39x slower                                                             |
| Geometric mean       | (ref)                                                      | 1.05x slower                                                                     |

Benchmark hidden because not significant (1): pickle_list

Benchmarks with tag 'startup':
==============================

| Benchmark      | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240419-linux-x86_64-faster%2dcpython-move_set_ip_to_exits-3.13.0a6+-ed60e2e |
|----------------|:----------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| python_startup | 10.8 ms                                                    | 10.5 ms: 1.02x faster                                                            |
| Geometric mean | (ref)                                                      | 1.01x faster                                                                     |

Benchmark hidden because not significant (1): python_startup_no_site

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240419-linux-x86_64-faster%2dcpython-move_set_ip_to_exits-3.13.0a6+-ed60e2e |
|-----------------|:----------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| genshi_text     | 23.7 ms                                                    | 26.7 ms: 1.13x slower                                                            |
| mako            | 11.2 ms                                                    | 13.7 ms: 1.22x slower                                                            |
| genshi_xml      | 51.6 ms                                                    | 63.1 ms: 1.22x slower                                                            |
| django_template | 34.8 ms                                                    | 42.8 ms: 1.23x slower                                                            |
| Geometric mean  | (ref)                                                      | 1.20x slower                                                                     |

All benchmarks:
===============

| Benchmark                  | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240419-linux-x86_64-faster%2dcpython-move_set_ip_to_exits-3.13.0a6+-ed60e2e |
|----------------------------|:----------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| typing_runtime_protocols   | 165 us                                                     | 129 us: 1.28x faster                                                             |
| xml_etree_parse            | 162 ms                                                     | 152 ms: 1.06x faster                                                             |
| gc_traversal               | 3.98 ms                                                    | 3.78 ms: 1.05x faster                                                            |
| json_loads                 | 28.9 us                                                    | 27.7 us: 1.04x faster                                                            |
| json                       | 5.31 ms                                                    | 5.13 ms: 1.03x faster                                                            |
| create_gc_cycles           | 1.82 ms                                                    | 1.77 ms: 1.03x faster                                                            |
| python_startup             | 10.8 ms                                                    | 10.5 ms: 1.02x faster                                                            |
| json_dumps                 | 10.7 ms                                                    | 10.7 ms: 1.01x faster                                                            |
| unpickle                   | 15.1 us                                                    | 15.1 us: 1.00x faster                                                            |
| regex_effbot               | 3.67 ms                                                    | 3.68 ms: 1.00x slower                                                            |
| deepcopy_reduce            | 3.35 us                                                    | 3.38 us: 1.01x slower                                                            |
| generators                 | 29.6 ms                                                    | 29.9 ms: 1.01x slower                                                            |
| asyncio_tcp                | 508 ms                                                     | 514 ms: 1.01x slower                                                             |
| pickle_dict                | 34.8 us                                                    | 35.2 us: 1.01x slower                                                            |
| asyncio_tcp_ssl            | 1.84 sec                                                   | 1.86 sec: 1.01x slower                                                           |
| pickle                     | 11.5 us                                                    | 11.6 us: 1.01x slower                                                            |
| pickle_pure_python         | 305 us                                                     | 310 us: 1.01x slower                                                             |
| logging_silent             | 105 ns                                                     | 107 ns: 1.02x slower                                                             |
| unpickle_list              | 5.34 us                                                    | 5.46 us: 1.02x slower                                                            |
| thrift                     | 823 us                                                     | 841 us: 1.02x slower                                                             |
| regex_dna                  | 221 ms                                                     | 227 ms: 1.03x slower                                                             |
| coroutines                 | 23.2 ms                                                    | 23.8 ms: 1.03x slower                                                            |
| xml_etree_iterparse        | 107 ms                                                     | 110 ms: 1.03x slower                                                             |
| async_tree_io              | 939 ms                                                     | 968 ms: 1.03x slower                                                             |
| regex_v8                   | 25.1 ms                                                    | 26.0 ms: 1.03x slower                                                            |
| dask                       | 369 ms                                                     | 383 ms: 1.04x slower                                                             |
| gunicorn                   | 1.28 ms                                                    | 1.33 ms: 1.04x slower                                                            |
| mdp                        | 2.79 sec                                                   | 2.90 sec: 1.04x slower                                                           |
| djangocms                  | 31.5 us                                                    | 32.9 us: 1.04x slower                                                            |
| pidigits                   | 191 ms                                                     | 200 ms: 1.05x slower                                                             |
| sqlite_synth               | 2.99 us                                                    | 3.14 us: 1.05x slower                                                            |
| aiohttp                    | 1.18 ms                                                    | 1.24 ms: 1.05x slower                                                            |
| async_tree_cpu_io_mixed    | 611 ms                                                     | 646 ms: 1.06x slower                                                             |
| deepcopy                   | 367 us                                                     | 390 us: 1.06x slower                                                             |
| coverage                   | 93.1 ms                                                    | 98.8 ms: 1.06x slower                                                            |
| xml_etree_process          | 61.2 ms                                                    | 65.0 ms: 1.06x slower                                                            |
| bench_thread_pool          | 834 us                                                     | 889 us: 1.07x slower                                                             |
| pathlib                    | 17.3 ms                                                    | 18.5 ms: 1.07x slower                                                            |
| async_tree_io_tg           | 936 ms                                                     | 1000 ms: 1.07x slower                                                            |
| async_tree_memoization_tg  | 444 ms                                                     | 476 ms: 1.07x slower                                                             |
| async_generators           | 442 ms                                                     | 479 ms: 1.08x slower                                                             |
| html5lib                   | 67.2 ms                                                    | 72.9 ms: 1.08x slower                                                            |
| async_tree_cpu_io_mixed_tg | 587 ms                                                     | 640 ms: 1.09x slower                                                             |
| async_tree_none_tg         | 336 ms                                                     | 367 ms: 1.09x slower                                                             |
| tornado_http               | 94.6 ms                                                    | 104 ms: 1.10x slower                                                             |
| pylint                     | 317 ms                                                     | 348 ms: 1.10x slower                                                             |
| xml_etree_generate         | 87.4 ms                                                    | 96.0 ms: 1.10x slower                                                            |
| mypy2                      | 742 ms                                                     | 817 ms: 1.10x slower                                                             |
| async_tree_memoization     | 463 ms                                                     | 511 ms: 1.10x slower                                                             |
| dulwich_log                | 67.2 ms                                                    | 74.3 ms: 1.11x slower                                                            |
| logging_format             | 6.47 us                                                    | 7.16 us: 1.11x slower                                                            |
| docutils                   | 2.83 sec                                                   | 3.15 sec: 1.11x slower                                                           |
| chameleon                  | 7.22 ms                                                    | 8.08 ms: 1.12x slower                                                            |
| logging_simple             | 5.74 us                                                    | 6.46 us: 1.12x slower                                                            |
| richards                   | 50.9 ms                                                    | 57.3 ms: 1.13x slower                                                            |
| genshi_text                | 23.7 ms                                                    | 26.7 ms: 1.13x slower                                                            |
| richards_super             | 57.4 ms                                                    | 65.0 ms: 1.13x slower                                                            |
| 2to3                       | 274 ms                                                     | 311 ms: 1.13x slower                                                             |
| scimark_fft                | 392 ms                                                     | 448 ms: 1.14x slower                                                             |
| telco                      | 8.41 ms                                                    | 9.60 ms: 1.14x slower                                                            |
| pycparser                  | 1.16 sec                                                   | 1.32 sec: 1.14x slower                                                           |
| sympy_integrate            | 20.5 ms                                                    | 23.5 ms: 1.15x slower                                                            |
| sqlglot_transpile          | 1.63 ms                                                    | 1.88 ms: 1.15x slower                                                            |
| sympy_sum                  | 156 ms                                                     | 180 ms: 1.16x slower                                                             |
| sympy_expand               | 473 ms                                                     | 546 ms: 1.16x slower                                                             |
| sqlglot_normalize          | 110 ms                                                     | 128 ms: 1.16x slower                                                             |
| sympy_str                  | 282 ms                                                     | 328 ms: 1.16x slower                                                             |
| deepcopy_memo              | 39.7 us                                                    | 46.3 us: 1.17x slower                                                            |
| sqlglot_parse              | 1.32 ms                                                    | 1.55 ms: 1.18x slower                                                            |
| float                      | 78.9 ms                                                    | 93.3 ms: 1.18x slower                                                            |
| sqlglot_optimize           | 55.5 ms                                                    | 65.9 ms: 1.19x slower                                                            |
| scimark_sor                | 127 ms                                                     | 151 ms: 1.19x slower                                                             |
| meteor_contest             | 110 ms                                                     | 131 ms: 1.19x slower                                                             |
| scimark_sparse_mat_mult    | 5.27 ms                                                    | 6.30 ms: 1.20x slower                                                            |
| spectral_norm              | 116 ms                                                     | 141 ms: 1.21x slower                                                             |
| mako                       | 11.2 ms                                                    | 13.7 ms: 1.22x slower                                                            |
| genshi_xml                 | 51.6 ms                                                    | 63.1 ms: 1.22x slower                                                            |
| django_template            | 34.8 ms                                                    | 42.8 ms: 1.23x slower                                                            |
| tomli_loads                | 2.12 sec                                                   | 2.69 sec: 1.27x slower                                                           |
| fannkuch                   | 402 ms                                                     | 515 ms: 1.28x slower                                                             |
| raytrace                   | 267 ms                                                     | 343 ms: 1.29x slower                                                             |
| crypto_pyaes               | 77.5 ms                                                    | 100 ms: 1.30x slower                                                             |
| deltablue                  | 3.25 ms                                                    | 4.23 ms: 1.30x slower                                                            |
| go                         | 145 ms                                                     | 191 ms: 1.32x slower                                                             |
| chaos                      | 61.3 ms                                                    | 83.3 ms: 1.36x slower                                                            |
| pyflate                    | 484 ms                                                     | 672 ms: 1.39x slower                                                             |
| unpickle_pure_python       | 218 us                                                     | 303 us: 1.39x slower                                                             |
| regex_compile              | 137 ms                                                     | 191 ms: 1.40x slower                                                             |
| pprint_safe_repr           | 758 ms                                                     | 1.07 sec: 1.41x slower                                                           |
| scimark_lu                 | 122 ms                                                     | 172 ms: 1.42x slower                                                             |
| nqueens                    | 81.4 ms                                                    | 117 ms: 1.43x slower                                                             |
| nbody                      | 88.3 ms                                                    | 127 ms: 1.44x slower                                                             |
| pprint_pformat             | 1.56 sec                                                   | 2.26 sec: 1.45x slower                                                           |
| comprehensions             | 16.6 us                                                    | 24.3 us: 1.46x slower                                                            |
| scimark_monte_carlo        | 69.2 ms                                                    | 106 ms: 1.53x slower                                                             |
| hexiom                     | 6.30 ms                                                    | 10.2 ms: 1.61x slower                                                            |
| Geometric mean             | (ref)                                                      | 1.12x slower                                                                     |

Benchmark hidden because not significant (5): python_startup_no_site, pickle_list, asyncio_websockets, bench_mp_pool, async_tree_none
Ignored benchmarks (2) of results/bm-20240605-3.13.0b2-3a83b17/bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17.json: bpe_tokeniser, flaskblogging

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.09x
- 95% likely to have a slowdown of 1.09x
- 99% likely to have a slowdown of 1.08x

# Memory
- memory change: 0.99x