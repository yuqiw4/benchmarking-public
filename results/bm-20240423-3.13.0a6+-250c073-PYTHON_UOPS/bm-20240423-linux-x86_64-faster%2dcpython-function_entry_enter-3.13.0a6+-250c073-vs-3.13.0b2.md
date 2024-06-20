# Results vs. 3.13.0b2

- fork: faster-cpython
- ref: function_entry_enter
- machine: linux-x86_64
- commit hash: 250c073
- commit date: 2024-04-23
- overall geometric mean: 1.10x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.06x slower
- Memory change: 1.00x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240423-linux-x86_64-faster%2dcpython-function_entry_enter-3.13.0a6+-250c073 |
|----------------|:----------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| 2to3           | 274 ms                                                     | 303 ms: 1.11x slower                                                             |
| chameleon      | 7.22 ms                                                    | 8.01 ms: 1.11x slower                                                            |
| docutils       | 2.83 sec                                                   | 3.09 sec: 1.09x slower                                                           |
| html5lib       | 67.2 ms                                                    | 71.8 ms: 1.07x slower                                                            |
| tornado_http   | 94.6 ms                                                    | 103 ms: 1.09x slower                                                             |
| Geometric mean | (ref)                                                      | 1.09x slower                                                                     |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240423-linux-x86_64-faster%2dcpython-function_entry_enter-3.13.0a6+-250c073 |
|----------------------------|:----------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| async_tree_io_tg           | 936 ms                                                     | 972 ms: 1.04x slower                                                             |
| async_tree_memoization_tg  | 444 ms                                                     | 463 ms: 1.04x slower                                                             |
| async_tree_cpu_io_mixed    | 611 ms                                                     | 638 ms: 1.04x slower                                                             |
| async_tree_none_tg         | 336 ms                                                     | 353 ms: 1.05x slower                                                             |
| async_tree_cpu_io_mixed_tg | 587 ms                                                     | 628 ms: 1.07x slower                                                             |
| async_tree_memoization     | 463 ms                                                     | 502 ms: 1.08x slower                                                             |
| Geometric mean             | (ref)                                                      | 1.04x slower                                                                     |

Benchmark hidden because not significant (2): async_tree_none, async_tree_io

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240423-linux-x86_64-faster%2dcpython-function_entry_enter-3.13.0a6+-250c073 |
|----------------|:----------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| pidigits       | 191 ms                                                     | 212 ms: 1.11x slower                                                             |
| float          | 78.9 ms                                                    | 91.1 ms: 1.16x slower                                                            |
| nbody          | 88.3 ms                                                    | 123 ms: 1.39x slower                                                             |
| Geometric mean | (ref)                                                      | 1.21x slower                                                                     |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240423-linux-x86_64-faster%2dcpython-function_entry_enter-3.13.0a6+-250c073 |
|----------------|:----------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| regex_dna      | 221 ms                                                     | 224 ms: 1.01x slower                                                             |
| regex_compile  | 137 ms                                                     | 182 ms: 1.33x slower                                                             |
| Geometric mean | (ref)                                                      | 1.08x slower                                                                     |

Benchmark hidden because not significant (2): regex_v8, regex_effbot

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240423-linux-x86_64-faster%2dcpython-function_entry_enter-3.13.0a6+-250c073 |
|----------------------|:----------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| xml_etree_parse      | 162 ms                                                     | 151 ms: 1.07x faster                                                             |
| json_loads           | 28.9 us                                                    | 28.2 us: 1.02x faster                                                            |
| unpickle_list        | 5.34 us                                                    | 5.41 us: 1.01x slower                                                            |
| json_dumps           | 10.7 ms                                                    | 10.9 ms: 1.01x slower                                                            |
| pickle_dict          | 34.8 us                                                    | 35.5 us: 1.02x slower                                                            |
| pickle               | 11.5 us                                                    | 11.9 us: 1.04x slower                                                            |
| unpickle             | 15.1 us                                                    | 15.7 us: 1.04x slower                                                            |
| pickle_pure_python   | 305 us                                                     | 318 us: 1.04x slower                                                             |
| xml_etree_iterparse  | 107 ms                                                     | 112 ms: 1.04x slower                                                             |
| xml_etree_process    | 61.2 ms                                                    | 64.0 ms: 1.05x slower                                                            |
| xml_etree_generate   | 87.4 ms                                                    | 92.9 ms: 1.06x slower                                                            |
| tomli_loads          | 2.12 sec                                                   | 2.53 sec: 1.19x slower                                                           |
| unpickle_pure_python | 218 us                                                     | 286 us: 1.31x slower                                                             |
| Geometric mean       | (ref)                                                      | 1.05x slower                                                                     |

Benchmark hidden because not significant (1): pickle_list

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240423-linux-x86_64-faster%2dcpython-function_entry_enter-3.13.0a6+-250c073 |
|------------------------|:----------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| python_startup         | 10.8 ms                                                    | 10.6 ms: 1.01x faster                                                            |
| python_startup_no_site | 7.11 ms                                                    | 7.18 ms: 1.01x slower                                                            |
| Geometric mean         | (ref)                                                      | 1.00x faster                                                                     |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240423-linux-x86_64-faster%2dcpython-function_entry_enter-3.13.0a6+-250c073 |
|-----------------|:----------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| genshi_text     | 23.7 ms                                                    | 25.2 ms: 1.07x slower                                                            |
| genshi_xml      | 51.6 ms                                                    | 59.0 ms: 1.14x slower                                                            |
| django_template | 34.8 ms                                                    | 40.9 ms: 1.17x slower                                                            |
| mako            | 11.2 ms                                                    | 13.7 ms: 1.22x slower                                                            |
| Geometric mean  | (ref)                                                      | 1.15x slower                                                                     |

All benchmarks:
===============

| Benchmark                  | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240423-linux-x86_64-faster%2dcpython-function_entry_enter-3.13.0a6+-250c073 |
|----------------------------|:----------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| typing_runtime_protocols   | 165 us                                                     | 123 us: 1.34x faster                                                             |
| xml_etree_parse            | 162 ms                                                     | 151 ms: 1.07x faster                                                             |
| json_loads                 | 28.9 us                                                    | 28.2 us: 1.02x faster                                                            |
| create_gc_cycles           | 1.82 ms                                                    | 1.78 ms: 1.02x faster                                                            |
| python_startup             | 10.8 ms                                                    | 10.6 ms: 1.01x faster                                                            |
| logging_silent             | 105 ns                                                     | 104 ns: 1.01x faster                                                             |
| gc_traversal               | 3.98 ms                                                    | 3.96 ms: 1.00x faster                                                            |
| thrift                     | 823 us                                                     | 827 us: 1.01x slower                                                             |
| bench_mp_pool              | 23.9 ms                                                    | 24.0 ms: 1.01x slower                                                            |
| python_startup_no_site     | 7.11 ms                                                    | 7.18 ms: 1.01x slower                                                            |
| unpickle_list              | 5.34 us                                                    | 5.41 us: 1.01x slower                                                            |
| regex_dna                  | 221 ms                                                     | 224 ms: 1.01x slower                                                             |
| json_dumps                 | 10.7 ms                                                    | 10.9 ms: 1.01x slower                                                            |
| asyncio_tcp_ssl            | 1.84 sec                                                   | 1.87 sec: 1.02x slower                                                           |
| generators                 | 29.6 ms                                                    | 30.2 ms: 1.02x slower                                                            |
| pickle_dict                | 34.8 us                                                    | 35.5 us: 1.02x slower                                                            |
| djangocms                  | 31.5 us                                                    | 32.5 us: 1.03x slower                                                            |
| coroutines                 | 23.2 ms                                                    | 24.0 ms: 1.03x slower                                                            |
| gunicorn                   | 1.28 ms                                                    | 1.33 ms: 1.04x slower                                                            |
| async_tree_io_tg           | 936 ms                                                     | 972 ms: 1.04x slower                                                             |
| pickle                     | 11.5 us                                                    | 11.9 us: 1.04x slower                                                            |
| asyncio_tcp                | 508 ms                                                     | 528 ms: 1.04x slower                                                             |
| deepcopy                   | 367 us                                                     | 381 us: 1.04x slower                                                             |
| unpickle                   | 15.1 us                                                    | 15.7 us: 1.04x slower                                                            |
| pickle_pure_python         | 305 us                                                     | 318 us: 1.04x slower                                                             |
| dask                       | 369 ms                                                     | 385 ms: 1.04x slower                                                             |
| async_tree_memoization_tg  | 444 ms                                                     | 463 ms: 1.04x slower                                                             |
| xml_etree_iterparse        | 107 ms                                                     | 112 ms: 1.04x slower                                                             |
| async_tree_cpu_io_mixed    | 611 ms                                                     | 638 ms: 1.04x slower                                                             |
| aiohttp                    | 1.18 ms                                                    | 1.23 ms: 1.04x slower                                                            |
| coverage                   | 93.1 ms                                                    | 97.3 ms: 1.04x slower                                                            |
| xml_etree_process          | 61.2 ms                                                    | 64.0 ms: 1.05x slower                                                            |
| async_tree_none_tg         | 336 ms                                                     | 353 ms: 1.05x slower                                                             |
| bench_thread_pool          | 834 us                                                     | 880 us: 1.06x slower                                                             |
| xml_etree_generate         | 87.4 ms                                                    | 92.9 ms: 1.06x slower                                                            |
| pathlib                    | 17.3 ms                                                    | 18.4 ms: 1.06x slower                                                            |
| genshi_text                | 23.7 ms                                                    | 25.2 ms: 1.07x slower                                                            |
| html5lib                   | 67.2 ms                                                    | 71.8 ms: 1.07x slower                                                            |
| async_tree_cpu_io_mixed_tg | 587 ms                                                     | 628 ms: 1.07x slower                                                             |
| async_generators           | 442 ms                                                     | 475 ms: 1.07x slower                                                             |
| async_tree_memoization     | 463 ms                                                     | 502 ms: 1.08x slower                                                             |
| richards_super             | 57.4 ms                                                    | 62.3 ms: 1.09x slower                                                            |
| dulwich_log                | 67.2 ms                                                    | 73.2 ms: 1.09x slower                                                            |
| richards                   | 50.9 ms                                                    | 55.6 ms: 1.09x slower                                                            |
| tornado_http               | 94.6 ms                                                    | 103 ms: 1.09x slower                                                             |
| docutils                   | 2.83 sec                                                   | 3.09 sec: 1.09x slower                                                           |
| pycparser                  | 1.16 sec                                                   | 1.27 sec: 1.10x slower                                                           |
| pylint                     | 317 ms                                                     | 349 ms: 1.10x slower                                                             |
| mypy2                      | 742 ms                                                     | 818 ms: 1.10x slower                                                             |
| 2to3                       | 274 ms                                                     | 303 ms: 1.11x slower                                                             |
| telco                      | 8.41 ms                                                    | 9.30 ms: 1.11x slower                                                            |
| pidigits                   | 191 ms                                                     | 212 ms: 1.11x slower                                                             |
| chameleon                  | 7.22 ms                                                    | 8.01 ms: 1.11x slower                                                            |
| meteor_contest             | 110 ms                                                     | 122 ms: 1.11x slower                                                             |
| sqlglot_transpile          | 1.63 ms                                                    | 1.82 ms: 1.11x slower                                                            |
| logging_simple             | 5.74 us                                                    | 6.40 us: 1.11x slower                                                            |
| deepcopy_memo              | 39.7 us                                                    | 44.6 us: 1.12x slower                                                            |
| logging_format             | 6.47 us                                                    | 7.28 us: 1.13x slower                                                            |
| sqlglot_parse              | 1.32 ms                                                    | 1.50 ms: 1.13x slower                                                            |
| sqlglot_normalize          | 110 ms                                                     | 125 ms: 1.14x slower                                                             |
| genshi_xml                 | 51.6 ms                                                    | 59.0 ms: 1.14x slower                                                            |
| sqlglot_optimize           | 55.5 ms                                                    | 63.5 ms: 1.14x slower                                                            |
| sympy_sum                  | 156 ms                                                     | 178 ms: 1.14x slower                                                             |
| sympy_str                  | 282 ms                                                     | 326 ms: 1.15x slower                                                             |
| float                      | 78.9 ms                                                    | 91.1 ms: 1.16x slower                                                            |
| scimark_sparse_mat_mult    | 5.27 ms                                                    | 6.12 ms: 1.16x slower                                                            |
| sympy_expand               | 473 ms                                                     | 550 ms: 1.16x slower                                                             |
| sympy_integrate            | 20.5 ms                                                    | 23.9 ms: 1.17x slower                                                            |
| scimark_fft                | 392 ms                                                     | 460 ms: 1.17x slower                                                             |
| django_template            | 34.8 ms                                                    | 40.9 ms: 1.17x slower                                                            |
| tomli_loads                | 2.12 sec                                                   | 2.53 sec: 1.19x slower                                                           |
| crypto_pyaes               | 77.5 ms                                                    | 92.5 ms: 1.19x slower                                                            |
| raytrace                   | 267 ms                                                     | 322 ms: 1.21x slower                                                             |
| mako                       | 11.2 ms                                                    | 13.7 ms: 1.22x slower                                                            |
| spectral_norm              | 116 ms                                                     | 142 ms: 1.22x slower                                                             |
| pyflate                    | 484 ms                                                     | 595 ms: 1.23x slower                                                             |
| scimark_sor                | 127 ms                                                     | 157 ms: 1.23x slower                                                             |
| fannkuch                   | 402 ms                                                     | 498 ms: 1.24x slower                                                             |
| pprint_safe_repr           | 758 ms                                                     | 952 ms: 1.26x slower                                                             |
| pprint_pformat             | 1.56 sec                                                   | 1.97 sec: 1.27x slower                                                           |
| chaos                      | 61.3 ms                                                    | 78.9 ms: 1.29x slower                                                            |
| deltablue                  | 3.25 ms                                                    | 4.21 ms: 1.30x slower                                                            |
| scimark_monte_carlo        | 69.2 ms                                                    | 90.5 ms: 1.31x slower                                                            |
| unpickle_pure_python       | 218 us                                                     | 286 us: 1.31x slower                                                             |
| nqueens                    | 81.4 ms                                                    | 108 ms: 1.32x slower                                                             |
| regex_compile              | 137 ms                                                     | 182 ms: 1.33x slower                                                             |
| go                         | 145 ms                                                     | 193 ms: 1.33x slower                                                             |
| scimark_lu                 | 122 ms                                                     | 168 ms: 1.38x slower                                                             |
| nbody                      | 88.3 ms                                                    | 123 ms: 1.39x slower                                                             |
| comprehensions             | 16.6 us                                                    | 23.2 us: 1.40x slower                                                            |
| hexiom                     | 6.30 ms                                                    | 9.53 ms: 1.51x slower                                                            |
| Geometric mean             | (ref)                                                      | 1.10x slower                                                                     |

Benchmark hidden because not significant (10): async_tree_none, regex_v8, json, mdp, sqlite_synth, regex_effbot, asyncio_websockets, pickle_list, deepcopy_reduce, async_tree_io
Ignored benchmarks (2) of results/bm-20240605-3.13.0b2-3a83b17/bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17.json: bpe_tokeniser, flaskblogging

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.08x
- 95% likely to have a slowdown of 1.07x
- 99% likely to have a slowdown of 1.06x

# Memory
- memory change: 1.00x