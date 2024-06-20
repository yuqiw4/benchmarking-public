# Results vs. 3.13.0b2

- fork: faster-cpython
- ref: unify_tier_2_for_ite
- machine: linux-x86_64
- commit hash: 04feb78
- commit date: 2024-04-30
- overall geometric mean: 1.12x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.08x slower
- Memory change: 0.99x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240430-linux-x86_64-faster%2dcpython-unify_tier_2_for_ite-3.13.0a6+-04feb78 |
|----------------|:----------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| 2to3           | 274 ms                                                     | 321 ms: 1.17x slower                                                             |
| chameleon      | 7.22 ms                                                    | 7.94 ms: 1.10x slower                                                            |
| docutils       | 2.83 sec                                                   | 3.19 sec: 1.13x slower                                                           |
| html5lib       | 67.2 ms                                                    | 76.3 ms: 1.14x slower                                                            |
| tornado_http   | 94.6 ms                                                    | 104 ms: 1.09x slower                                                             |
| Geometric mean | (ref)                                                      | 1.13x slower                                                                     |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240430-linux-x86_64-faster%2dcpython-unify_tier_2_for_ite-3.13.0a6+-04feb78 |
|----------------------------|:----------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| async_tree_cpu_io_mixed    | 611 ms                                                     | 633 ms: 1.04x slower                                                             |
| async_tree_none_tg         | 336 ms                                                     | 350 ms: 1.04x slower                                                             |
| async_tree_cpu_io_mixed_tg | 587 ms                                                     | 620 ms: 1.06x slower                                                             |
| async_tree_memoization     | 463 ms                                                     | 499 ms: 1.08x slower                                                             |
| Geometric mean             | (ref)                                                      | 1.03x slower                                                                     |

Benchmark hidden because not significant (4): async_tree_none, async_tree_io_tg, async_tree_io, async_tree_memoization_tg

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240430-linux-x86_64-faster%2dcpython-unify_tier_2_for_ite-3.13.0a6+-04feb78 |
|----------------|:----------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| pidigits       | 191 ms                                                     | 213 ms: 1.11x slower                                                             |
| float          | 78.9 ms                                                    | 91.9 ms: 1.16x slower                                                            |
| nbody          | 88.3 ms                                                    | 125 ms: 1.41x slower                                                             |
| Geometric mean | (ref)                                                      | 1.22x slower                                                                     |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240430-linux-x86_64-faster%2dcpython-unify_tier_2_for_ite-3.13.0a6+-04feb78 |
|----------------|:----------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| regex_v8       | 25.1 ms                                                    | 25.0 ms: 1.01x faster                                                            |
| regex_effbot   | 3.67 ms                                                    | 3.68 ms: 1.00x slower                                                            |
| regex_compile  | 137 ms                                                     | 181 ms: 1.32x slower                                                             |
| Geometric mean | (ref)                                                      | 1.07x slower                                                                     |

Benchmark hidden because not significant (1): regex_dna

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240430-linux-x86_64-faster%2dcpython-unify_tier_2_for_ite-3.13.0a6+-04feb78 |
|----------------------|:----------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| xml_etree_parse      | 162 ms                                                     | 153 ms: 1.06x faster                                                             |
| json_loads           | 28.9 us                                                    | 27.7 us: 1.04x faster                                                            |
| pickle_list          | 5.11 us                                                    | 5.02 us: 1.02x faster                                                            |
| unpickle_list        | 5.34 us                                                    | 5.28 us: 1.01x faster                                                            |
| pickle_dict          | 34.8 us                                                    | 35.2 us: 1.01x slower                                                            |
| xml_etree_iterparse  | 107 ms                                                     | 111 ms: 1.03x slower                                                             |
| pickle_pure_python   | 305 us                                                     | 321 us: 1.05x slower                                                             |
| pickle               | 11.5 us                                                    | 12.1 us: 1.06x slower                                                            |
| unpickle             | 15.1 us                                                    | 16.5 us: 1.09x slower                                                            |
| xml_etree_generate   | 87.4 ms                                                    | 96.3 ms: 1.10x slower                                                            |
| xml_etree_process    | 61.2 ms                                                    | 67.5 ms: 1.10x slower                                                            |
| tomli_loads          | 2.12 sec                                                   | 2.54 sec: 1.20x slower                                                           |
| unpickle_pure_python | 218 us                                                     | 286 us: 1.31x slower                                                             |
| Geometric mean       | (ref)                                                      | 1.06x slower                                                                     |

Benchmark hidden because not significant (1): json_dumps

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240430-linux-x86_64-faster%2dcpython-unify_tier_2_for_ite-3.13.0a6+-04feb78 |
|------------------------|:----------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| python_startup         | 10.8 ms                                                    | 10.6 ms: 1.01x faster                                                            |
| python_startup_no_site | 7.11 ms                                                    | 7.17 ms: 1.01x slower                                                            |
| Geometric mean         | (ref)                                                      | 1.00x faster                                                                     |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240430-linux-x86_64-faster%2dcpython-unify_tier_2_for_ite-3.13.0a6+-04feb78 |
|-----------------|:----------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| django_template | 34.8 ms                                                    | 40.7 ms: 1.17x slower                                                            |
| mako            | 11.2 ms                                                    | 14.0 ms: 1.24x slower                                                            |
| genshi_text     | 23.7 ms                                                    | 31.2 ms: 1.32x slower                                                            |
| genshi_xml      | 51.6 ms                                                    | 70.8 ms: 1.37x slower                                                            |
| Geometric mean  | (ref)                                                      | 1.27x slower                                                                     |

All benchmarks:
===============

| Benchmark                  | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240430-linux-x86_64-faster%2dcpython-unify_tier_2_for_ite-3.13.0a6+-04feb78 |
|----------------------------|:----------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| xml_etree_parse            | 162 ms                                                     | 153 ms: 1.06x faster                                                             |
| json_loads                 | 28.9 us                                                    | 27.7 us: 1.04x faster                                                            |
| json                       | 5.31 ms                                                    | 5.16 ms: 1.03x faster                                                            |
| create_gc_cycles           | 1.82 ms                                                    | 1.78 ms: 1.02x faster                                                            |
| pickle_list                | 5.11 us                                                    | 5.02 us: 1.02x faster                                                            |
| python_startup             | 10.8 ms                                                    | 10.6 ms: 1.01x faster                                                            |
| unpickle_list              | 5.34 us                                                    | 5.28 us: 1.01x faster                                                            |
| regex_v8                   | 25.1 ms                                                    | 25.0 ms: 1.01x faster                                                            |
| regex_effbot               | 3.67 ms                                                    | 3.68 ms: 1.00x slower                                                            |
| deepcopy_reduce            | 3.35 us                                                    | 3.38 us: 1.01x slower                                                            |
| python_startup_no_site     | 7.11 ms                                                    | 7.17 ms: 1.01x slower                                                            |
| thrift                     | 823 us                                                     | 831 us: 1.01x slower                                                             |
| mdp                        | 2.79 sec                                                   | 2.82 sec: 1.01x slower                                                           |
| pickle_dict                | 34.8 us                                                    | 35.2 us: 1.01x slower                                                            |
| sqlite_synth               | 2.99 us                                                    | 3.03 us: 1.01x slower                                                            |
| asyncio_tcp_ssl            | 1.84 sec                                                   | 1.87 sec: 1.02x slower                                                           |
| gc_traversal               | 3.98 ms                                                    | 4.06 ms: 1.02x slower                                                            |
| logging_silent             | 105 ns                                                     | 108 ns: 1.03x slower                                                             |
| xml_etree_iterparse        | 107 ms                                                     | 111 ms: 1.03x slower                                                             |
| async_tree_cpu_io_mixed    | 611 ms                                                     | 633 ms: 1.04x slower                                                             |
| asyncio_tcp                | 508 ms                                                     | 528 ms: 1.04x slower                                                             |
| async_tree_none_tg         | 336 ms                                                     | 350 ms: 1.04x slower                                                             |
| dask                       | 369 ms                                                     | 386 ms: 1.05x slower                                                             |
| coroutines                 | 23.2 ms                                                    | 24.3 ms: 1.05x slower                                                            |
| djangocms                  | 31.5 us                                                    | 33.0 us: 1.05x slower                                                            |
| pathlib                    | 17.3 ms                                                    | 18.2 ms: 1.05x slower                                                            |
| pickle_pure_python         | 305 us                                                     | 321 us: 1.05x slower                                                             |
| generators                 | 29.6 ms                                                    | 31.2 ms: 1.05x slower                                                            |
| async_tree_cpu_io_mixed_tg | 587 ms                                                     | 620 ms: 1.06x slower                                                             |
| gunicorn                   | 1.28 ms                                                    | 1.35 ms: 1.06x slower                                                            |
| pickle                     | 11.5 us                                                    | 12.1 us: 1.06x slower                                                            |
| deepcopy                   | 367 us                                                     | 389 us: 1.06x slower                                                             |
| aiohttp                    | 1.18 ms                                                    | 1.26 ms: 1.07x slower                                                            |
| async_generators           | 442 ms                                                     | 476 ms: 1.08x slower                                                             |
| async_tree_memoization     | 463 ms                                                     | 499 ms: 1.08x slower                                                             |
| unpickle                   | 15.1 us                                                    | 16.5 us: 1.09x slower                                                            |
| bench_thread_pool          | 834 us                                                     | 912 us: 1.09x slower                                                             |
| tornado_http               | 94.6 ms                                                    | 104 ms: 1.09x slower                                                             |
| logging_format             | 6.47 us                                                    | 7.09 us: 1.10x slower                                                            |
| chameleon                  | 7.22 ms                                                    | 7.94 ms: 1.10x slower                                                            |
| xml_etree_generate         | 87.4 ms                                                    | 96.3 ms: 1.10x slower                                                            |
| xml_etree_process          | 61.2 ms                                                    | 67.5 ms: 1.10x slower                                                            |
| pycparser                  | 1.16 sec                                                   | 1.28 sec: 1.10x slower                                                           |
| telco                      | 8.41 ms                                                    | 9.32 ms: 1.11x slower                                                            |
| meteor_contest             | 110 ms                                                     | 122 ms: 1.11x slower                                                             |
| pidigits                   | 191 ms                                                     | 213 ms: 1.11x slower                                                             |
| sqlglot_transpile          | 1.63 ms                                                    | 1.82 ms: 1.12x slower                                                            |
| dulwich_log                | 67.2 ms                                                    | 75.1 ms: 1.12x slower                                                            |
| logging_simple             | 5.74 us                                                    | 6.44 us: 1.12x slower                                                            |
| docutils                   | 2.83 sec                                                   | 3.19 sec: 1.13x slower                                                           |
| sqlglot_parse              | 1.32 ms                                                    | 1.49 ms: 1.13x slower                                                            |
| scimark_sparse_mat_mult    | 5.27 ms                                                    | 5.97 ms: 1.13x slower                                                            |
| scimark_fft                | 392 ms                                                     | 445 ms: 1.13x slower                                                             |
| html5lib                   | 67.2 ms                                                    | 76.3 ms: 1.14x slower                                                            |
| mypy2                      | 742 ms                                                     | 842 ms: 1.14x slower                                                             |
| deepcopy_memo              | 39.7 us                                                    | 45.5 us: 1.15x slower                                                            |
| sympy_sum                  | 156 ms                                                     | 179 ms: 1.15x slower                                                             |
| pylint                     | 317 ms                                                     | 365 ms: 1.15x slower                                                             |
| typing_runtime_protocols   | 165 us                                                     | 190 us: 1.15x slower                                                             |
| crypto_pyaes               | 77.5 ms                                                    | 89.6 ms: 1.16x slower                                                            |
| richards_super             | 57.4 ms                                                    | 66.5 ms: 1.16x slower                                                            |
| float                      | 78.9 ms                                                    | 91.9 ms: 1.16x slower                                                            |
| django_template            | 34.8 ms                                                    | 40.7 ms: 1.17x slower                                                            |
| sqlglot_optimize           | 55.5 ms                                                    | 65.0 ms: 1.17x slower                                                            |
| sqlglot_normalize          | 110 ms                                                     | 129 ms: 1.17x slower                                                             |
| richards                   | 50.9 ms                                                    | 59.7 ms: 1.17x slower                                                            |
| 2to3                       | 274 ms                                                     | 321 ms: 1.17x slower                                                             |
| sympy_str                  | 282 ms                                                     | 332 ms: 1.17x slower                                                             |
| spectral_norm              | 116 ms                                                     | 137 ms: 1.18x slower                                                             |
| sympy_integrate            | 20.5 ms                                                    | 24.2 ms: 1.18x slower                                                            |
| sympy_expand               | 473 ms                                                     | 561 ms: 1.19x slower                                                             |
| fannkuch                   | 402 ms                                                     | 481 ms: 1.20x slower                                                             |
| tomli_loads                | 2.12 sec                                                   | 2.54 sec: 1.20x slower                                                           |
| pyflate                    | 484 ms                                                     | 595 ms: 1.23x slower                                                             |
| mako                       | 11.2 ms                                                    | 14.0 ms: 1.24x slower                                                            |
| scimark_sor                | 127 ms                                                     | 159 ms: 1.25x slower                                                             |
| raytrace                   | 267 ms                                                     | 334 ms: 1.25x slower                                                             |
| pprint_safe_repr           | 758 ms                                                     | 965 ms: 1.27x slower                                                             |
| chaos                      | 61.3 ms                                                    | 78.6 ms: 1.28x slower                                                            |
| pprint_pformat             | 1.56 sec                                                   | 2.00 sec: 1.28x slower                                                           |
| scimark_monte_carlo        | 69.2 ms                                                    | 89.5 ms: 1.29x slower                                                            |
| unpickle_pure_python       | 218 us                                                     | 286 us: 1.31x slower                                                             |
| deltablue                  | 3.25 ms                                                    | 4.29 ms: 1.32x slower                                                            |
| genshi_text                | 23.7 ms                                                    | 31.2 ms: 1.32x slower                                                            |
| regex_compile              | 137 ms                                                     | 181 ms: 1.32x slower                                                             |
| nqueens                    | 81.4 ms                                                    | 109 ms: 1.33x slower                                                             |
| genshi_xml                 | 51.6 ms                                                    | 70.8 ms: 1.37x slower                                                            |
| scimark_lu                 | 122 ms                                                     | 168 ms: 1.38x slower                                                             |
| go                         | 145 ms                                                     | 203 ms: 1.41x slower                                                             |
| nbody                      | 88.3 ms                                                    | 125 ms: 1.41x slower                                                             |
| comprehensions             | 16.6 us                                                    | 24.6 us: 1.48x slower                                                            |
| hexiom                     | 6.30 ms                                                    | 9.77 ms: 1.55x slower                                                            |
| Geometric mean             | (ref)                                                      | 1.12x slower                                                                     |

Benchmark hidden because not significant (9): async_tree_none, json_dumps, regex_dna, asyncio_websockets, bench_mp_pool, coverage, async_tree_io_tg, async_tree_io, async_tree_memoization_tg
Ignored benchmarks (2) of results/bm-20240605-3.13.0b2-3a83b17/bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17.json: bpe_tokeniser, flaskblogging

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.10x
- 95% likely to have a slowdown of 1.09x
- 99% likely to have a slowdown of 1.08x

# Memory
- memory change: 0.99x