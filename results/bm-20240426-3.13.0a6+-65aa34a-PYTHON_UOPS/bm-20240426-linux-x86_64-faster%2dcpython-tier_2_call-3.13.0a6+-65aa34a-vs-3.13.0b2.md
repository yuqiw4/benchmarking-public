# Results vs. 3.13.0b2

- fork: faster-cpython
- ref: tier_2_call
- machine: linux-x86_64
- commit hash: 65aa34a
- commit date: 2024-04-26
- overall geometric mean: 1.12x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.06x slower
- Memory change: 0.99x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240426-linux-x86_64-faster%2dcpython-tier_2_call-3.13.0a6+-65aa34a |
|----------------|:----------------------------------------------------------:|:-----------------------------------------------------------------------:|
| 2to3           | 274 ms                                                     | 305 ms: 1.11x slower                                                    |
| chameleon      | 7.22 ms                                                    | 7.57 ms: 1.05x slower                                                   |
| html5lib       | 67.2 ms                                                    | 72.7 ms: 1.08x slower                                                   |
| tornado_http   | 94.6 ms                                                    | 102 ms: 1.08x slower                                                    |
| Geometric mean | (ref)                                                      | 1.08x slower                                                            |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240426-linux-x86_64-faster%2dcpython-tier_2_call-3.13.0a6+-65aa34a |
|----------------------------|:----------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_none_tg         | 336 ms                                                     | 347 ms: 1.03x slower                                                    |
| async_tree_memoization_tg  | 444 ms                                                     | 459 ms: 1.04x slower                                                    |
| async_tree_cpu_io_mixed    | 611 ms                                                     | 634 ms: 1.04x slower                                                    |
| async_tree_cpu_io_mixed_tg | 587 ms                                                     | 619 ms: 1.05x slower                                                    |
| async_tree_memoization     | 463 ms                                                     | 503 ms: 1.09x slower                                                    |
| Geometric mean             | (ref)                                                      | 1.03x slower                                                            |

Benchmark hidden because not significant (3): async_tree_none, async_tree_io, async_tree_io_tg

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240426-linux-x86_64-faster%2dcpython-tier_2_call-3.13.0a6+-65aa34a |
|----------------|:----------------------------------------------------------:|:-----------------------------------------------------------------------:|
| pidigits       | 191 ms                                                     | 191 ms: 1.00x faster                                                    |
| float          | 78.9 ms                                                    | 91.7 ms: 1.16x slower                                                   |
| nbody          | 88.3 ms                                                    | 129 ms: 1.46x slower                                                    |
| Geometric mean | (ref)                                                      | 1.19x slower                                                            |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240426-linux-x86_64-faster%2dcpython-tier_2_call-3.13.0a6+-65aa34a |
|----------------|:----------------------------------------------------------:|:-----------------------------------------------------------------------:|
| regex_v8       | 25.1 ms                                                    | 24.8 ms: 1.01x faster                                                   |
| regex_effbot   | 3.67 ms                                                    | 3.70 ms: 1.01x slower                                                   |
| regex_dna      | 221 ms                                                     | 224 ms: 1.01x slower                                                    |
| regex_compile  | 137 ms                                                     | 182 ms: 1.33x slower                                                    |
| Geometric mean | (ref)                                                      | 1.08x slower                                                            |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240426-linux-x86_64-faster%2dcpython-tier_2_call-3.13.0a6+-65aa34a |
|----------------------|:----------------------------------------------------------:|:-----------------------------------------------------------------------:|
| xml_etree_parse      | 162 ms                                                     | 151 ms: 1.07x faster                                                    |
| json_loads           | 28.9 us                                                    | 27.7 us: 1.04x faster                                                   |
| unpickle_list        | 5.34 us                                                    | 5.17 us: 1.03x faster                                                   |
| pickle_list          | 5.11 us                                                    | 5.15 us: 1.01x slower                                                   |
| pickle_dict          | 34.8 us                                                    | 35.2 us: 1.01x slower                                                   |
| unpickle             | 15.1 us                                                    | 15.4 us: 1.02x slower                                                   |
| xml_etree_iterparse  | 107 ms                                                     | 110 ms: 1.03x slower                                                    |
| pickle_pure_python   | 305 us                                                     | 321 us: 1.05x slower                                                    |
| pickle               | 11.5 us                                                    | 12.1 us: 1.05x slower                                                   |
| xml_etree_generate   | 87.4 ms                                                    | 92.7 ms: 1.06x slower                                                   |
| xml_etree_process    | 61.2 ms                                                    | 65.2 ms: 1.07x slower                                                   |
| tomli_loads          | 2.12 sec                                                   | 2.54 sec: 1.20x slower                                                  |
| unpickle_pure_python | 218 us                                                     | 295 us: 1.35x slower                                                    |
| Geometric mean       | (ref)                                                      | 1.05x slower                                                            |

Benchmark hidden because not significant (1): json_dumps

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240426-linux-x86_64-faster%2dcpython-tier_2_call-3.13.0a6+-65aa34a |
|------------------------|:----------------------------------------------------------:|:-----------------------------------------------------------------------:|
| python_startup         | 10.8 ms                                                    | 10.5 ms: 1.02x faster                                                   |
| python_startup_no_site | 7.11 ms                                                    | 7.13 ms: 1.00x slower                                                   |
| Geometric mean         | (ref)                                                      | 1.01x faster                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240426-linux-x86_64-faster%2dcpython-tier_2_call-3.13.0a6+-65aa34a |
|-----------------|:----------------------------------------------------------:|:-----------------------------------------------------------------------:|
| django_template | 34.8 ms                                                    | 41.4 ms: 1.19x slower                                                   |
| genshi_text     | 23.7 ms                                                    | 28.9 ms: 1.22x slower                                                   |
| mako            | 11.2 ms                                                    | 13.9 ms: 1.23x slower                                                   |
| genshi_xml      | 51.6 ms                                                    | 65.5 ms: 1.27x slower                                                   |
| Geometric mean  | (ref)                                                      | 1.23x slower                                                            |

All benchmarks:
===============

| Benchmark                  | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240426-linux-x86_64-faster%2dcpython-tier_2_call-3.13.0a6+-65aa34a |
|----------------------------|:----------------------------------------------------------:|:-----------------------------------------------------------------------:|
| xml_etree_parse            | 162 ms                                                     | 151 ms: 1.07x faster                                                    |
| json_loads                 | 28.9 us                                                    | 27.7 us: 1.04x faster                                                   |
| logging_silent             | 105 ns                                                     | 101 ns: 1.04x faster                                                    |
| unpickle_list              | 5.34 us                                                    | 5.17 us: 1.03x faster                                                   |
| python_startup             | 10.8 ms                                                    | 10.5 ms: 1.02x faster                                                   |
| create_gc_cycles           | 1.82 ms                                                    | 1.78 ms: 1.02x faster                                                   |
| json                       | 5.31 ms                                                    | 5.23 ms: 1.01x faster                                                   |
| regex_v8                   | 25.1 ms                                                    | 24.8 ms: 1.01x faster                                                   |
| pidigits                   | 191 ms                                                     | 191 ms: 1.00x faster                                                    |
| python_startup_no_site     | 7.11 ms                                                    | 7.13 ms: 1.00x slower                                                   |
| pickle_list                | 5.11 us                                                    | 5.15 us: 1.01x slower                                                   |
| regex_effbot               | 3.67 ms                                                    | 3.70 ms: 1.01x slower                                                   |
| pickle_dict                | 34.8 us                                                    | 35.2 us: 1.01x slower                                                   |
| thrift                     | 823 us                                                     | 833 us: 1.01x slower                                                    |
| regex_dna                  | 221 ms                                                     | 224 ms: 1.01x slower                                                    |
| unpickle                   | 15.1 us                                                    | 15.4 us: 1.02x slower                                                   |
| asyncio_tcp_ssl            | 1.84 sec                                                   | 1.87 sec: 1.02x slower                                                  |
| gc_traversal               | 3.98 ms                                                    | 4.05 ms: 1.02x slower                                                   |
| deepcopy_reduce            | 3.35 us                                                    | 3.41 us: 1.02x slower                                                   |
| sqlite_synth               | 2.99 us                                                    | 3.06 us: 1.02x slower                                                   |
| xml_etree_iterparse        | 107 ms                                                     | 110 ms: 1.03x slower                                                    |
| async_tree_none_tg         | 336 ms                                                     | 347 ms: 1.03x slower                                                    |
| djangocms                  | 31.5 us                                                    | 32.6 us: 1.03x slower                                                   |
| async_tree_memoization_tg  | 444 ms                                                     | 459 ms: 1.04x slower                                                    |
| async_tree_cpu_io_mixed    | 611 ms                                                     | 634 ms: 1.04x slower                                                    |
| asyncio_tcp                | 508 ms                                                     | 530 ms: 1.04x slower                                                    |
| gunicorn                   | 1.28 ms                                                    | 1.34 ms: 1.05x slower                                                   |
| coverage                   | 93.1 ms                                                    | 97.6 ms: 1.05x slower                                                   |
| chameleon                  | 7.22 ms                                                    | 7.57 ms: 1.05x slower                                                   |
| coroutines                 | 23.2 ms                                                    | 24.3 ms: 1.05x slower                                                   |
| pickle_pure_python         | 305 us                                                     | 321 us: 1.05x slower                                                    |
| aiohttp                    | 1.18 ms                                                    | 1.24 ms: 1.05x slower                                                   |
| async_tree_cpu_io_mixed_tg | 587 ms                                                     | 619 ms: 1.05x slower                                                    |
| pickle                     | 11.5 us                                                    | 12.1 us: 1.05x slower                                                   |
| dask                       | 369 ms                                                     | 390 ms: 1.06x slower                                                    |
| xml_etree_generate         | 87.4 ms                                                    | 92.7 ms: 1.06x slower                                                   |
| pathlib                    | 17.3 ms                                                    | 18.5 ms: 1.07x slower                                                   |
| xml_etree_process          | 61.2 ms                                                    | 65.2 ms: 1.07x slower                                                   |
| async_generators           | 442 ms                                                     | 477 ms: 1.08x slower                                                    |
| mdp                        | 2.79 sec                                                   | 3.01 sec: 1.08x slower                                                  |
| html5lib                   | 67.2 ms                                                    | 72.7 ms: 1.08x slower                                                   |
| bench_thread_pool          | 834 us                                                     | 902 us: 1.08x slower                                                    |
| tornado_http               | 94.6 ms                                                    | 102 ms: 1.08x slower                                                    |
| async_tree_memoization     | 463 ms                                                     | 503 ms: 1.09x slower                                                    |
| deepcopy                   | 367 us                                                     | 401 us: 1.09x slower                                                    |
| dulwich_log                | 67.2 ms                                                    | 73.9 ms: 1.10x slower                                                   |
| pycparser                  | 1.16 sec                                                   | 1.28 sec: 1.10x slower                                                  |
| richards_super             | 57.4 ms                                                    | 63.5 ms: 1.11x slower                                                   |
| telco                      | 8.41 ms                                                    | 9.32 ms: 1.11x slower                                                   |
| richards                   | 50.9 ms                                                    | 56.7 ms: 1.11x slower                                                   |
| 2to3                       | 274 ms                                                     | 305 ms: 1.11x slower                                                    |
| meteor_contest             | 110 ms                                                     | 123 ms: 1.12x slower                                                    |
| sqlglot_transpile          | 1.63 ms                                                    | 1.85 ms: 1.13x slower                                                   |
| sqlglot_parse              | 1.32 ms                                                    | 1.52 ms: 1.15x slower                                                   |
| sympy_sum                  | 156 ms                                                     | 180 ms: 1.16x slower                                                    |
| scimark_fft                | 392 ms                                                     | 454 ms: 1.16x slower                                                    |
| sympy_expand               | 473 ms                                                     | 549 ms: 1.16x slower                                                    |
| float                      | 78.9 ms                                                    | 91.7 ms: 1.16x slower                                                   |
| sympy_integrate            | 20.5 ms                                                    | 23.8 ms: 1.16x slower                                                   |
| sqlglot_normalize          | 110 ms                                                     | 129 ms: 1.17x slower                                                    |
| sympy_str                  | 282 ms                                                     | 331 ms: 1.17x slower                                                    |
| sqlglot_optimize           | 55.5 ms                                                    | 65.3 ms: 1.18x slower                                                   |
| logging_format             | 6.47 us                                                    | 7.66 us: 1.18x slower                                                   |
| typing_runtime_protocols   | 165 us                                                     | 196 us: 1.19x slower                                                    |
| django_template            | 34.8 ms                                                    | 41.4 ms: 1.19x slower                                                   |
| deepcopy_memo              | 39.7 us                                                    | 47.3 us: 1.19x slower                                                   |
| scimark_sparse_mat_mult    | 5.27 ms                                                    | 6.32 ms: 1.20x slower                                                   |
| tomli_loads                | 2.12 sec                                                   | 2.54 sec: 1.20x slower                                                  |
| logging_simple             | 5.74 us                                                    | 6.90 us: 1.20x slower                                                   |
| crypto_pyaes               | 77.5 ms                                                    | 93.6 ms: 1.21x slower                                                   |
| genshi_text                | 23.7 ms                                                    | 28.9 ms: 1.22x slower                                                   |
| pyflate                    | 484 ms                                                     | 592 ms: 1.22x slower                                                    |
| mako                       | 11.2 ms                                                    | 13.9 ms: 1.23x slower                                                   |
| scimark_sor                | 127 ms                                                     | 157 ms: 1.24x slower                                                    |
| raytrace                   | 267 ms                                                     | 330 ms: 1.24x slower                                                    |
| fannkuch                   | 402 ms                                                     | 499 ms: 1.24x slower                                                    |
| spectral_norm              | 116 ms                                                     | 144 ms: 1.24x slower                                                    |
| pprint_safe_repr           | 758 ms                                                     | 953 ms: 1.26x slower                                                    |
| genshi_xml                 | 51.6 ms                                                    | 65.5 ms: 1.27x slower                                                   |
| pprint_pformat             | 1.56 sec                                                   | 1.98 sec: 1.27x slower                                                  |
| chaos                      | 61.3 ms                                                    | 79.8 ms: 1.30x slower                                                   |
| regex_compile              | 137 ms                                                     | 182 ms: 1.33x slower                                                    |
| scimark_monte_carlo        | 69.2 ms                                                    | 92.1 ms: 1.33x slower                                                   |
| unpickle_pure_python       | 218 us                                                     | 295 us: 1.35x slower                                                    |
| nqueens                    | 81.4 ms                                                    | 111 ms: 1.36x slower                                                    |
| deltablue                  | 3.25 ms                                                    | 4.45 ms: 1.37x slower                                                   |
| scimark_lu                 | 122 ms                                                     | 168 ms: 1.38x slower                                                    |
| nbody                      | 88.3 ms                                                    | 129 ms: 1.46x slower                                                    |
| go                         | 145 ms                                                     | 212 ms: 1.47x slower                                                    |
| comprehensions             | 16.6 us                                                    | 24.7 us: 1.49x slower                                                   |
| hexiom                     | 6.30 ms                                                    | 10.2 ms: 1.62x slower                                                   |
| Geometric mean             | (ref)                                                      | 1.12x slower                                                            |

Benchmark hidden because not significant (7): async_tree_none, generators, asyncio_websockets, json_dumps, bench_mp_pool, async_tree_io, async_tree_io_tg
Ignored benchmarks (5) of results/bm-20240605-3.13.0b2-3a83b17/bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17.json: bpe_tokeniser, docutils, flaskblogging, mypy2, pylint

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.08x
- 95% likely to have a slowdown of 1.07x
- 99% likely to have a slowdown of 1.06x

# Memory
- memory change: 0.99x