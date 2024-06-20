# Results vs. 3.13.0b2

- fork: faster-cpython
- ref: function_entry_enter
- machine: linux-x86_64
- commit hash: d04d9ac
- commit date: 2024-04-23
- overall geometric mean: 1.12x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.08x slower
- Memory change: 1.00x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240423-linux-x86_64-faster%2dcpython-function_entry_enter-3.13.0a6+-d04d9ac |
|----------------|:----------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| 2to3           | 274 ms                                                     | 306 ms: 1.12x slower                                                             |
| chameleon      | 7.22 ms                                                    | 8.10 ms: 1.12x slower                                                            |
| docutils       | 2.83 sec                                                   | 3.13 sec: 1.11x slower                                                           |
| html5lib       | 67.2 ms                                                    | 73.3 ms: 1.09x slower                                                            |
| tornado_http   | 94.6 ms                                                    | 103 ms: 1.09x slower                                                             |
| Geometric mean | (ref)                                                      | 1.11x slower                                                                     |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240423-linux-x86_64-faster%2dcpython-function_entry_enter-3.13.0a6+-d04d9ac |
|----------------------------|:----------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| async_tree_io_tg           | 936 ms                                                     | 971 ms: 1.04x slower                                                             |
| async_tree_io              | 939 ms                                                     | 975 ms: 1.04x slower                                                             |
| async_tree_cpu_io_mixed    | 611 ms                                                     | 638 ms: 1.04x slower                                                             |
| async_tree_memoization_tg  | 444 ms                                                     | 467 ms: 1.05x slower                                                             |
| async_tree_none_tg         | 336 ms                                                     | 356 ms: 1.06x slower                                                             |
| async_tree_cpu_io_mixed_tg | 587 ms                                                     | 626 ms: 1.07x slower                                                             |
| async_tree_memoization     | 463 ms                                                     | 508 ms: 1.10x slower                                                             |
| Geometric mean             | (ref)                                                      | 1.05x slower                                                                     |

Benchmark hidden because not significant (1): async_tree_none

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240423-linux-x86_64-faster%2dcpython-function_entry_enter-3.13.0a6+-d04d9ac |
|----------------|:----------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| pidigits       | 191 ms                                                     | 199 ms: 1.04x slower                                                             |
| float          | 78.9 ms                                                    | 94.9 ms: 1.20x slower                                                            |
| nbody          | 88.3 ms                                                    | 128 ms: 1.45x slower                                                             |
| Geometric mean | (ref)                                                      | 1.22x slower                                                                     |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240423-linux-x86_64-faster%2dcpython-function_entry_enter-3.13.0a6+-d04d9ac |
|----------------|:----------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| regex_effbot   | 3.67 ms                                                    | 3.69 ms: 1.00x slower                                                            |
| regex_v8       | 25.1 ms                                                    | 25.5 ms: 1.02x slower                                                            |
| regex_dna      | 221 ms                                                     | 227 ms: 1.03x slower                                                             |
| regex_compile  | 137 ms                                                     | 186 ms: 1.36x slower                                                             |
| Geometric mean | (ref)                                                      | 1.09x slower                                                                     |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240423-linux-x86_64-faster%2dcpython-function_entry_enter-3.13.0a6+-d04d9ac |
|----------------------|:----------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| xml_etree_parse      | 162 ms                                                     | 150 ms: 1.08x faster                                                             |
| json_loads           | 28.9 us                                                    | 27.8 us: 1.04x faster                                                            |
| pickle_list          | 5.11 us                                                    | 5.08 us: 1.01x faster                                                            |
| json_dumps           | 10.7 ms                                                    | 10.8 ms: 1.01x slower                                                            |
| unpickle             | 15.1 us                                                    | 15.3 us: 1.01x slower                                                            |
| pickle_dict          | 34.8 us                                                    | 35.5 us: 1.02x slower                                                            |
| pickle               | 11.5 us                                                    | 11.9 us: 1.03x slower                                                            |
| pickle_pure_python   | 305 us                                                     | 321 us: 1.05x slower                                                             |
| xml_etree_iterparse  | 107 ms                                                     | 114 ms: 1.07x slower                                                             |
| xml_etree_process    | 61.2 ms                                                    | 65.6 ms: 1.07x slower                                                            |
| xml_etree_generate   | 87.4 ms                                                    | 95.3 ms: 1.09x slower                                                            |
| tomli_loads          | 2.12 sec                                                   | 2.62 sec: 1.24x slower                                                           |
| unpickle_pure_python | 218 us                                                     | 298 us: 1.37x slower                                                             |
| Geometric mean       | (ref)                                                      | 1.05x slower                                                                     |

Benchmark hidden because not significant (1): unpickle_list

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240423-linux-x86_64-faster%2dcpython-function_entry_enter-3.13.0a6+-d04d9ac |
|------------------------|:----------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| python_startup         | 10.8 ms                                                    | 10.6 ms: 1.01x faster                                                            |
| python_startup_no_site | 7.11 ms                                                    | 7.14 ms: 1.01x slower                                                            |
| Geometric mean         | (ref)                                                      | 1.00x faster                                                                     |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240423-linux-x86_64-faster%2dcpython-function_entry_enter-3.13.0a6+-d04d9ac |
|-----------------|:----------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| genshi_text     | 23.7 ms                                                    | 25.7 ms: 1.08x slower                                                            |
| genshi_xml      | 51.6 ms                                                    | 59.9 ms: 1.16x slower                                                            |
| django_template | 34.8 ms                                                    | 41.5 ms: 1.19x slower                                                            |
| mako            | 11.2 ms                                                    | 14.5 ms: 1.29x slower                                                            |
| Geometric mean  | (ref)                                                      | 1.18x slower                                                                     |

All benchmarks:
===============

| Benchmark                  | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240423-linux-x86_64-faster%2dcpython-function_entry_enter-3.13.0a6+-d04d9ac |
|----------------------------|:----------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| typing_runtime_protocols   | 165 us                                                     | 128 us: 1.29x faster                                                             |
| xml_etree_parse            | 162 ms                                                     | 150 ms: 1.08x faster                                                             |
| json_loads                 | 28.9 us                                                    | 27.8 us: 1.04x faster                                                            |
| json                       | 5.31 ms                                                    | 5.20 ms: 1.02x faster                                                            |
| python_startup             | 10.8 ms                                                    | 10.6 ms: 1.01x faster                                                            |
| create_gc_cycles           | 1.82 ms                                                    | 1.79 ms: 1.01x faster                                                            |
| pickle_list                | 5.11 us                                                    | 5.08 us: 1.01x faster                                                            |
| gc_traversal               | 3.98 ms                                                    | 3.96 ms: 1.00x faster                                                            |
| regex_effbot               | 3.67 ms                                                    | 3.69 ms: 1.00x slower                                                            |
| python_startup_no_site     | 7.11 ms                                                    | 7.14 ms: 1.01x slower                                                            |
| sqlite_synth               | 2.99 us                                                    | 3.01 us: 1.01x slower                                                            |
| json_dumps                 | 10.7 ms                                                    | 10.8 ms: 1.01x slower                                                            |
| bench_mp_pool              | 23.9 ms                                                    | 24.1 ms: 1.01x slower                                                            |
| unpickle                   | 15.1 us                                                    | 15.3 us: 1.01x slower                                                            |
| regex_v8                   | 25.1 ms                                                    | 25.5 ms: 1.02x slower                                                            |
| pickle_dict                | 34.8 us                                                    | 35.5 us: 1.02x slower                                                            |
| asyncio_tcp_ssl            | 1.84 sec                                                   | 1.88 sec: 1.02x slower                                                           |
| thrift                     | 823 us                                                     | 841 us: 1.02x slower                                                             |
| generators                 | 29.6 ms                                                    | 30.3 ms: 1.02x slower                                                            |
| regex_dna                  | 221 ms                                                     | 227 ms: 1.03x slower                                                             |
| pickle                     | 11.5 us                                                    | 11.9 us: 1.03x slower                                                            |
| gunicorn                   | 1.28 ms                                                    | 1.32 ms: 1.04x slower                                                            |
| async_tree_io_tg           | 936 ms                                                     | 971 ms: 1.04x slower                                                             |
| asyncio_tcp                | 508 ms                                                     | 528 ms: 1.04x slower                                                             |
| async_tree_io              | 939 ms                                                     | 975 ms: 1.04x slower                                                             |
| dask                       | 369 ms                                                     | 384 ms: 1.04x slower                                                             |
| pidigits                   | 191 ms                                                     | 199 ms: 1.04x slower                                                             |
| async_tree_cpu_io_mixed    | 611 ms                                                     | 638 ms: 1.04x slower                                                             |
| coroutines                 | 23.2 ms                                                    | 24.2 ms: 1.04x slower                                                            |
| coverage                   | 93.1 ms                                                    | 97.4 ms: 1.05x slower                                                            |
| logging_silent             | 105 ns                                                     | 110 ns: 1.05x slower                                                             |
| aiohttp                    | 1.18 ms                                                    | 1.23 ms: 1.05x slower                                                            |
| deepcopy                   | 367 us                                                     | 384 us: 1.05x slower                                                             |
| djangocms                  | 31.5 us                                                    | 33.0 us: 1.05x slower                                                            |
| pickle_pure_python         | 305 us                                                     | 321 us: 1.05x slower                                                             |
| async_tree_memoization_tg  | 444 ms                                                     | 467 ms: 1.05x slower                                                             |
| async_tree_none_tg         | 336 ms                                                     | 356 ms: 1.06x slower                                                             |
| pathlib                    | 17.3 ms                                                    | 18.4 ms: 1.06x slower                                                            |
| xml_etree_iterparse        | 107 ms                                                     | 114 ms: 1.07x slower                                                             |
| async_tree_cpu_io_mixed_tg | 587 ms                                                     | 626 ms: 1.07x slower                                                             |
| bench_thread_pool          | 834 us                                                     | 892 us: 1.07x slower                                                             |
| xml_etree_process          | 61.2 ms                                                    | 65.6 ms: 1.07x slower                                                            |
| genshi_text                | 23.7 ms                                                    | 25.7 ms: 1.08x slower                                                            |
| mdp                        | 2.79 sec                                                   | 3.02 sec: 1.08x slower                                                           |
| html5lib                   | 67.2 ms                                                    | 73.3 ms: 1.09x slower                                                            |
| xml_etree_generate         | 87.4 ms                                                    | 95.3 ms: 1.09x slower                                                            |
| async_generators           | 442 ms                                                     | 482 ms: 1.09x slower                                                             |
| tornado_http               | 94.6 ms                                                    | 103 ms: 1.09x slower                                                             |
| async_tree_memoization     | 463 ms                                                     | 508 ms: 1.10x slower                                                             |
| dulwich_log                | 67.2 ms                                                    | 73.9 ms: 1.10x slower                                                            |
| docutils                   | 2.83 sec                                                   | 3.13 sec: 1.11x slower                                                           |
| logging_format             | 6.47 us                                                    | 7.16 us: 1.11x slower                                                            |
| pylint                     | 317 ms                                                     | 351 ms: 1.11x slower                                                             |
| mypy2                      | 742 ms                                                     | 821 ms: 1.11x slower                                                             |
| richards_super             | 57.4 ms                                                    | 63.7 ms: 1.11x slower                                                            |
| telco                      | 8.41 ms                                                    | 9.36 ms: 1.11x slower                                                            |
| sqlglot_transpile          | 1.63 ms                                                    | 1.82 ms: 1.11x slower                                                            |
| meteor_contest             | 110 ms                                                     | 122 ms: 1.11x slower                                                             |
| pycparser                  | 1.16 sec                                                   | 1.29 sec: 1.11x slower                                                           |
| 2to3                       | 274 ms                                                     | 306 ms: 1.12x slower                                                             |
| logging_simple             | 5.74 us                                                    | 6.43 us: 1.12x slower                                                            |
| chameleon                  | 7.22 ms                                                    | 8.10 ms: 1.12x slower                                                            |
| richards                   | 50.9 ms                                                    | 57.3 ms: 1.12x slower                                                            |
| sqlglot_parse              | 1.32 ms                                                    | 1.50 ms: 1.14x slower                                                            |
| sympy_sum                  | 156 ms                                                     | 178 ms: 1.14x slower                                                             |
| sqlglot_normalize          | 110 ms                                                     | 126 ms: 1.14x slower                                                             |
| genshi_xml                 | 51.6 ms                                                    | 59.9 ms: 1.16x slower                                                            |
| deepcopy_memo              | 39.7 us                                                    | 46.1 us: 1.16x slower                                                            |
| sqlglot_optimize           | 55.5 ms                                                    | 64.5 ms: 1.16x slower                                                            |
| sympy_expand               | 473 ms                                                     | 552 ms: 1.17x slower                                                             |
| sympy_str                  | 282 ms                                                     | 330 ms: 1.17x slower                                                             |
| sympy_integrate            | 20.5 ms                                                    | 24.1 ms: 1.18x slower                                                            |
| django_template            | 34.8 ms                                                    | 41.5 ms: 1.19x slower                                                            |
| float                      | 78.9 ms                                                    | 94.9 ms: 1.20x slower                                                            |
| scimark_fft                | 392 ms                                                     | 473 ms: 1.20x slower                                                             |
| crypto_pyaes               | 77.5 ms                                                    | 95.3 ms: 1.23x slower                                                            |
| tomli_loads                | 2.12 sec                                                   | 2.62 sec: 1.24x slower                                                           |
| raytrace                   | 267 ms                                                     | 330 ms: 1.24x slower                                                             |
| scimark_sparse_mat_mult    | 5.27 ms                                                    | 6.54 ms: 1.24x slower                                                            |
| scimark_sor                | 127 ms                                                     | 161 ms: 1.26x slower                                                             |
| fannkuch                   | 402 ms                                                     | 511 ms: 1.27x slower                                                             |
| mako                       | 11.2 ms                                                    | 14.5 ms: 1.29x slower                                                            |
| pprint_safe_repr           | 758 ms                                                     | 983 ms: 1.30x slower                                                             |
| pprint_pformat             | 1.56 sec                                                   | 2.04 sec: 1.31x slower                                                           |
| chaos                      | 61.3 ms                                                    | 80.9 ms: 1.32x slower                                                            |
| spectral_norm              | 116 ms                                                     | 153 ms: 1.32x slower                                                             |
| pyflate                    | 484 ms                                                     | 639 ms: 1.32x slower                                                             |
| deltablue                  | 3.25 ms                                                    | 4.33 ms: 1.33x slower                                                            |
| scimark_monte_carlo        | 69.2 ms                                                    | 93.9 ms: 1.36x slower                                                            |
| regex_compile              | 137 ms                                                     | 186 ms: 1.36x slower                                                             |
| unpickle_pure_python       | 218 us                                                     | 298 us: 1.37x slower                                                             |
| nqueens                    | 81.4 ms                                                    | 111 ms: 1.37x slower                                                             |
| go                         | 145 ms                                                     | 201 ms: 1.39x slower                                                             |
| scimark_lu                 | 122 ms                                                     | 170 ms: 1.40x slower                                                             |
| nbody                      | 88.3 ms                                                    | 128 ms: 1.45x slower                                                             |
| comprehensions             | 16.6 us                                                    | 24.6 us: 1.48x slower                                                            |
| hexiom                     | 6.30 ms                                                    | 10.1 ms: 1.60x slower                                                            |
| Geometric mean             | (ref)                                                      | 1.12x slower                                                                     |

Benchmark hidden because not significant (4): asyncio_websockets, deepcopy_reduce, unpickle_list, async_tree_none
Ignored benchmarks (2) of results/bm-20240605-3.13.0b2-3a83b17/bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17.json: bpe_tokeniser, flaskblogging

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.09x
- 95% likely to have a slowdown of 1.08x
- 99% likely to have a slowdown of 1.08x

# Memory
- memory change: 1.00x