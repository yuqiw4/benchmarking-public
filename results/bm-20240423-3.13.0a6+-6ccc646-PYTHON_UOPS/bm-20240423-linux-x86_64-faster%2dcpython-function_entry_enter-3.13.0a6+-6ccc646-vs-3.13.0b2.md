# Results vs. 3.13.0b2

- fork: faster-cpython
- ref: function_entry_enter
- machine: linux-x86_64
- commit hash: 6ccc646
- commit date: 2024-04-23
- overall geometric mean: 1.28x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.21x slower
- Memory change: 1.00x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240423-linux-x86_64-faster%2dcpython-function_entry_enter-3.13.0a6+-6ccc646 |
|----------------|:----------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| 2to3           | 274 ms                                                     | 352 ms: 1.29x slower                                                             |
| chameleon      | 7.22 ms                                                    | 10.0 ms: 1.39x slower                                                            |
| docutils       | 2.83 sec                                                   | 3.61 sec: 1.28x slower                                                           |
| html5lib       | 67.2 ms                                                    | 103 ms: 1.53x slower                                                             |
| tornado_http   | 94.6 ms                                                    | 136 ms: 1.43x slower                                                             |
| Geometric mean | (ref)                                                      | 1.38x slower                                                                     |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240423-linux-x86_64-faster%2dcpython-function_entry_enter-3.13.0a6+-6ccc646 |
|----------------------------|:----------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| async_tree_io              | 939 ms                                                     | 1.11 sec: 1.19x slower                                                           |
| async_tree_cpu_io_mixed    | 611 ms                                                     | 734 ms: 1.20x slower                                                             |
| async_tree_none            | 378 ms                                                     | 457 ms: 1.21x slower                                                             |
| async_tree_io_tg           | 936 ms                                                     | 1.14 sec: 1.21x slower                                                           |
| async_tree_cpu_io_mixed_tg | 587 ms                                                     | 714 ms: 1.21x slower                                                             |
| async_tree_memoization_tg  | 444 ms                                                     | 564 ms: 1.27x slower                                                             |
| async_tree_none_tg         | 336 ms                                                     | 429 ms: 1.27x slower                                                             |
| async_tree_memoization     | 463 ms                                                     | 608 ms: 1.31x slower                                                             |
| Geometric mean             | (ref)                                                      | 1.23x slower                                                                     |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240423-linux-x86_64-faster%2dcpython-function_entry_enter-3.13.0a6+-6ccc646 |
|----------------|:----------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| pidigits       | 191 ms                                                     | 194 ms: 1.01x slower                                                             |
| float          | 78.9 ms                                                    | 94.3 ms: 1.20x slower                                                            |
| nbody          | 88.3 ms                                                    | 122 ms: 1.39x slower                                                             |
| Geometric mean | (ref)                                                      | 1.19x slower                                                                     |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240423-linux-x86_64-faster%2dcpython-function_entry_enter-3.13.0a6+-6ccc646 |
|----------------|:----------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| regex_effbot   | 3.67 ms                                                    | 3.72 ms: 1.01x slower                                                            |
| regex_v8       | 25.1 ms                                                    | 25.6 ms: 1.02x slower                                                            |
| regex_dna      | 221 ms                                                     | 227 ms: 1.03x slower                                                             |
| regex_compile  | 137 ms                                                     | 231 ms: 1.69x slower                                                             |
| Geometric mean | (ref)                                                      | 1.16x slower                                                                     |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240423-linux-x86_64-faster%2dcpython-function_entry_enter-3.13.0a6+-6ccc646 |
|----------------------|:----------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| xml_etree_parse      | 162 ms                                                     | 155 ms: 1.04x faster                                                             |
| json_loads           | 28.9 us                                                    | 28.5 us: 1.01x faster                                                            |
| pickle_list          | 5.11 us                                                    | 5.17 us: 1.01x slower                                                            |
| unpickle_list        | 5.34 us                                                    | 5.42 us: 1.01x slower                                                            |
| pickle_dict          | 34.8 us                                                    | 35.4 us: 1.02x slower                                                            |
| unpickle             | 15.1 us                                                    | 15.8 us: 1.04x slower                                                            |
| xml_etree_iterparse  | 107 ms                                                     | 112 ms: 1.05x slower                                                             |
| pickle               | 11.5 us                                                    | 12.0 us: 1.05x slower                                                            |
| json_dumps           | 10.7 ms                                                    | 12.7 ms: 1.18x slower                                                            |
| xml_etree_generate   | 87.4 ms                                                    | 111 ms: 1.27x slower                                                             |
| xml_etree_process    | 61.2 ms                                                    | 81.4 ms: 1.33x slower                                                            |
| tomli_loads          | 2.12 sec                                                   | 2.99 sec: 1.41x slower                                                           |
| unpickle_pure_python | 218 us                                                     | 337 us: 1.55x slower                                                             |
| pickle_pure_python   | 305 us                                                     | 500 us: 1.64x slower                                                             |
| Geometric mean       | (ref)                                                      | 1.16x slower                                                                     |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240423-linux-x86_64-faster%2dcpython-function_entry_enter-3.13.0a6+-6ccc646 |
|------------------------|:----------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| python_startup         | 10.8 ms                                                    | 10.7 ms: 1.01x faster                                                            |
| python_startup_no_site | 7.11 ms                                                    | 7.18 ms: 1.01x slower                                                            |
| Geometric mean         | (ref)                                                      | 1.00x slower                                                                     |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240423-linux-x86_64-faster%2dcpython-function_entry_enter-3.13.0a6+-6ccc646 |
|-----------------|:----------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| mako            | 11.2 ms                                                    | 13.8 ms: 1.23x slower                                                            |
| genshi_text     | 23.7 ms                                                    | 32.4 ms: 1.37x slower                                                            |
| genshi_xml      | 51.6 ms                                                    | 74.2 ms: 1.44x slower                                                            |
| django_template | 34.8 ms                                                    | 60.9 ms: 1.75x slower                                                            |
| Geometric mean  | (ref)                                                      | 1.43x slower                                                                     |

All benchmarks:
===============

| Benchmark                  | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240423-linux-x86_64-faster%2dcpython-function_entry_enter-3.13.0a6+-6ccc646 |
|----------------------------|:----------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| typing_runtime_protocols   | 165 us                                                     | 154 us: 1.07x faster                                                             |
| xml_etree_parse            | 162 ms                                                     | 155 ms: 1.04x faster                                                             |
| json_loads                 | 28.9 us                                                    | 28.5 us: 1.01x faster                                                            |
| python_startup             | 10.8 ms                                                    | 10.7 ms: 1.01x faster                                                            |
| create_gc_cycles           | 1.82 ms                                                    | 1.80 ms: 1.01x faster                                                            |
| asyncio_websockets         | 567 ms                                                     | 571 ms: 1.01x slower                                                             |
| python_startup_no_site     | 7.11 ms                                                    | 7.18 ms: 1.01x slower                                                            |
| pidigits                   | 191 ms                                                     | 194 ms: 1.01x slower                                                             |
| pickle_list                | 5.11 us                                                    | 5.17 us: 1.01x slower                                                            |
| regex_effbot               | 3.67 ms                                                    | 3.72 ms: 1.01x slower                                                            |
| unpickle_list              | 5.34 us                                                    | 5.42 us: 1.01x slower                                                            |
| gc_traversal               | 3.98 ms                                                    | 4.03 ms: 1.01x slower                                                            |
| pickle_dict                | 34.8 us                                                    | 35.4 us: 1.02x slower                                                            |
| regex_v8                   | 25.1 ms                                                    | 25.6 ms: 1.02x slower                                                            |
| json                       | 5.31 ms                                                    | 5.42 ms: 1.02x slower                                                            |
| regex_dna                  | 221 ms                                                     | 227 ms: 1.03x slower                                                             |
| asyncio_tcp_ssl            | 1.84 sec                                                   | 1.91 sec: 1.04x slower                                                           |
| unpickle                   | 15.1 us                                                    | 15.8 us: 1.04x slower                                                            |
| bench_mp_pool              | 23.9 ms                                                    | 25.0 ms: 1.05x slower                                                            |
| xml_etree_iterparse        | 107 ms                                                     | 112 ms: 1.05x slower                                                             |
| pickle                     | 11.5 us                                                    | 12.0 us: 1.05x slower                                                            |
| coverage                   | 93.1 ms                                                    | 98.5 ms: 1.06x slower                                                            |
| sqlite_synth               | 2.99 us                                                    | 3.16 us: 1.06x slower                                                            |
| generators                 | 29.6 ms                                                    | 31.7 ms: 1.07x slower                                                            |
| mdp                        | 2.79 sec                                                   | 2.99 sec: 1.07x slower                                                           |
| coroutines                 | 23.2 ms                                                    | 25.5 ms: 1.10x slower                                                            |
| asyncio_tcp                | 508 ms                                                     | 569 ms: 1.12x slower                                                             |
| meteor_contest             | 110 ms                                                     | 123 ms: 1.12x slower                                                             |
| async_generators           | 442 ms                                                     | 504 ms: 1.14x slower                                                             |
| telco                      | 8.41 ms                                                    | 9.65 ms: 1.15x slower                                                            |
| djangocms                  | 31.5 us                                                    | 36.5 us: 1.16x slower                                                            |
| scimark_fft                | 392 ms                                                     | 458 ms: 1.17x slower                                                             |
| scimark_sparse_mat_mult    | 5.27 ms                                                    | 6.19 ms: 1.17x slower                                                            |
| json_dumps                 | 10.7 ms                                                    | 12.7 ms: 1.18x slower                                                            |
| async_tree_io              | 939 ms                                                     | 1.11 sec: 1.19x slower                                                           |
| float                      | 78.9 ms                                                    | 94.3 ms: 1.20x slower                                                            |
| bench_thread_pool          | 834 us                                                     | 998 us: 1.20x slower                                                             |
| async_tree_cpu_io_mixed    | 611 ms                                                     | 734 ms: 1.20x slower                                                             |
| pathlib                    | 17.3 ms                                                    | 20.8 ms: 1.20x slower                                                            |
| crypto_pyaes               | 77.5 ms                                                    | 93.4 ms: 1.21x slower                                                            |
| async_tree_none            | 378 ms                                                     | 457 ms: 1.21x slower                                                             |
| async_tree_io_tg           | 936 ms                                                     | 1.14 sec: 1.21x slower                                                           |
| async_tree_cpu_io_mixed_tg | 587 ms                                                     | 714 ms: 1.21x slower                                                             |
| mako                       | 11.2 ms                                                    | 13.8 ms: 1.23x slower                                                            |
| spectral_norm              | 116 ms                                                     | 144 ms: 1.24x slower                                                             |
| fannkuch                   | 402 ms                                                     | 505 ms: 1.26x slower                                                             |
| gunicorn                   | 1.28 ms                                                    | 1.61 ms: 1.26x slower                                                            |
| xml_etree_generate         | 87.4 ms                                                    | 111 ms: 1.27x slower                                                             |
| async_tree_memoization_tg  | 444 ms                                                     | 564 ms: 1.27x slower                                                             |
| aiohttp                    | 1.18 ms                                                    | 1.50 ms: 1.27x slower                                                            |
| async_tree_none_tg         | 336 ms                                                     | 429 ms: 1.27x slower                                                             |
| docutils                   | 2.83 sec                                                   | 3.61 sec: 1.28x slower                                                           |
| 2to3                       | 274 ms                                                     | 352 ms: 1.29x slower                                                             |
| dask                       | 369 ms                                                     | 481 ms: 1.30x slower                                                             |
| thrift                     | 823 us                                                     | 1.08 ms: 1.31x slower                                                            |
| pylint                     | 317 ms                                                     | 416 ms: 1.31x slower                                                             |
| async_tree_memoization     | 463 ms                                                     | 608 ms: 1.31x slower                                                             |
| xml_etree_process          | 61.2 ms                                                    | 81.4 ms: 1.33x slower                                                            |
| mypy2                      | 742 ms                                                     | 994 ms: 1.34x slower                                                             |
| scimark_monte_carlo        | 69.2 ms                                                    | 93.1 ms: 1.35x slower                                                            |
| pyflate                    | 484 ms                                                     | 652 ms: 1.35x slower                                                             |
| genshi_text                | 23.7 ms                                                    | 32.4 ms: 1.37x slower                                                            |
| sympy_integrate            | 20.5 ms                                                    | 28.3 ms: 1.38x slower                                                            |
| deepcopy_memo              | 39.7 us                                                    | 55.0 us: 1.38x slower                                                            |
| sympy_sum                  | 156 ms                                                     | 216 ms: 1.39x slower                                                             |
| nbody                      | 88.3 ms                                                    | 122 ms: 1.39x slower                                                             |
| chameleon                  | 7.22 ms                                                    | 10.0 ms: 1.39x slower                                                            |
| pycparser                  | 1.16 sec                                                   | 1.61 sec: 1.39x slower                                                           |
| dulwich_log                | 67.2 ms                                                    | 93.7 ms: 1.40x slower                                                            |
| logging_silent             | 105 ns                                                     | 147 ns: 1.41x slower                                                             |
| tomli_loads                | 2.12 sec                                                   | 2.99 sec: 1.41x slower                                                           |
| sympy_str                  | 282 ms                                                     | 403 ms: 1.43x slower                                                             |
| tornado_http               | 94.6 ms                                                    | 136 ms: 1.43x slower                                                             |
| sympy_expand               | 473 ms                                                     | 679 ms: 1.44x slower                                                             |
| genshi_xml                 | 51.6 ms                                                    | 74.2 ms: 1.44x slower                                                            |
| sqlglot_optimize           | 55.5 ms                                                    | 81.2 ms: 1.46x slower                                                            |
| richards_super             | 57.4 ms                                                    | 84.5 ms: 1.47x slower                                                            |
| richards                   | 50.9 ms                                                    | 76.0 ms: 1.49x slower                                                            |
| deepcopy                   | 367 us                                                     | 553 us: 1.51x slower                                                             |
| sqlglot_normalize          | 110 ms                                                     | 166 ms: 1.51x slower                                                             |
| comprehensions             | 16.6 us                                                    | 25.2 us: 1.52x slower                                                            |
| deepcopy_reduce            | 3.35 us                                                    | 5.09 us: 1.52x slower                                                            |
| html5lib                   | 67.2 ms                                                    | 103 ms: 1.53x slower                                                             |
| sqlglot_transpile          | 1.63 ms                                                    | 2.52 ms: 1.54x slower                                                            |
| sqlglot_parse              | 1.32 ms                                                    | 2.04 ms: 1.55x slower                                                            |
| unpickle_pure_python       | 218 us                                                     | 337 us: 1.55x slower                                                             |
| scimark_sor                | 127 ms                                                     | 199 ms: 1.56x slower                                                             |
| scimark_lu                 | 122 ms                                                     | 190 ms: 1.56x slower                                                             |
| go                         | 145 ms                                                     | 230 ms: 1.59x slower                                                             |
| pickle_pure_python         | 305 us                                                     | 500 us: 1.64x slower                                                             |
| pprint_safe_repr           | 758 ms                                                     | 1.24 sec: 1.64x slower                                                           |
| pprint_pformat             | 1.56 sec                                                   | 2.58 sec: 1.66x slower                                                           |
| chaos                      | 61.3 ms                                                    | 103 ms: 1.68x slower                                                             |
| regex_compile              | 137 ms                                                     | 231 ms: 1.69x slower                                                             |
| nqueens                    | 81.4 ms                                                    | 139 ms: 1.71x slower                                                             |
| hexiom                     | 6.30 ms                                                    | 10.8 ms: 1.72x slower                                                            |
| django_template            | 34.8 ms                                                    | 60.9 ms: 1.75x slower                                                            |
| raytrace                   | 267 ms                                                     | 474 ms: 1.78x slower                                                             |
| logging_format             | 6.47 us                                                    | 11.7 us: 1.80x slower                                                            |
| logging_simple             | 5.74 us                                                    | 10.5 us: 1.84x slower                                                            |
| deltablue                  | 3.25 ms                                                    | 6.30 ms: 1.94x slower                                                            |
| Geometric mean             | (ref)                                                      | 1.28x slower                                                                     |
Ignored benchmarks (2) of results/bm-20240605-3.13.0b2-3a83b17/bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17.json: bpe_tokeniser, flaskblogging

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.25x
- 95% likely to have a slowdown of 1.24x
- 99% likely to have a slowdown of 1.21x

# Memory
- memory change: 1.00x