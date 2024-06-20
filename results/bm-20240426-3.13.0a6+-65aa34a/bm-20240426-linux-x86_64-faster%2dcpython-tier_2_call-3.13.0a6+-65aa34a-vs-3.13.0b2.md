# Results vs. 3.13.0b2

- fork: faster-cpython
- ref: tier_2_call
- machine: linux-x86_64
- commit hash: 65aa34a
- commit date: 2024-04-26
- overall geometric mean: 1.01x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.00x faster
- Memory change: 0.98x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240426-linux-x86_64-faster%2dcpython-tier_2_call-3.13.0a6+-65aa34a |
|----------------|:----------------------------------------------------------:|:-----------------------------------------------------------------------:|
| 2to3           | 274 ms                                                     | 267 ms: 1.02x faster                                                    |
| chameleon      | 7.22 ms                                                    | 6.96 ms: 1.04x faster                                                   |
| docutils       | 2.83 sec                                                   | 2.80 sec: 1.01x faster                                                  |
| html5lib       | 67.2 ms                                                    | 65.6 ms: 1.03x faster                                                   |
| tornado_http   | 94.6 ms                                                    | 94.4 ms: 1.00x faster                                                   |
| Geometric mean | (ref)                                                      | 1.02x faster                                                            |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240426-linux-x86_64-faster%2dcpython-tier_2_call-3.13.0a6+-65aa34a |
|----------------------------|:----------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_none            | 378 ms                                                     | 352 ms: 1.08x faster                                                    |
| async_tree_none_tg         | 336 ms                                                     | 330 ms: 1.02x faster                                                    |
| async_tree_cpu_io_mixed_tg | 587 ms                                                     | 609 ms: 1.04x slower                                                    |
| Geometric mean             | (ref)                                                      | 1.01x faster                                                            |

Benchmark hidden because not significant (5): async_tree_io, async_tree_memoization_tg, async_tree_io_tg, async_tree_memoization, async_tree_cpu_io_mixed

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240426-linux-x86_64-faster%2dcpython-tier_2_call-3.13.0a6+-65aa34a |
|----------------|:----------------------------------------------------------:|:-----------------------------------------------------------------------:|
| nbody          | 88.3 ms                                                    | 87.4 ms: 1.01x faster                                                   |
| pidigits       | 191 ms                                                     | 194 ms: 1.01x slower                                                    |
| Geometric mean | (ref)                                                      | 1.00x slower                                                            |

Benchmark hidden because not significant (1): float

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240426-linux-x86_64-faster%2dcpython-tier_2_call-3.13.0a6+-65aa34a |
|----------------|:----------------------------------------------------------:|:-----------------------------------------------------------------------:|
| regex_compile  | 137 ms                                                     | 134 ms: 1.02x faster                                                    |
| regex_effbot   | 3.67 ms                                                    | 3.85 ms: 1.05x slower                                                   |
| regex_v8       | 25.1 ms                                                    | 26.3 ms: 1.05x slower                                                   |
| regex_dna      | 221 ms                                                     | 232 ms: 1.05x slower                                                    |
| Geometric mean | (ref)                                                      | 1.03x slower                                                            |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240426-linux-x86_64-faster%2dcpython-tier_2_call-3.13.0a6+-65aa34a |
|----------------------|:----------------------------------------------------------:|:-----------------------------------------------------------------------:|
| json_loads           | 28.9 us                                                    | 27.4 us: 1.05x faster                                                   |
| unpickle_list        | 5.34 us                                                    | 5.19 us: 1.03x faster                                                   |
| unpickle_pure_python | 218 us                                                     | 213 us: 1.02x faster                                                    |
| pickle_pure_python   | 305 us                                                     | 299 us: 1.02x faster                                                    |
| xml_etree_process    | 61.2 ms                                                    | 60.2 ms: 1.02x faster                                                   |
| xml_etree_parse      | 162 ms                                                     | 159 ms: 1.02x faster                                                    |
| json_dumps           | 10.7 ms                                                    | 10.6 ms: 1.01x faster                                                   |
| pickle_dict          | 34.8 us                                                    | 34.4 us: 1.01x faster                                                   |
| xml_etree_generate   | 87.4 ms                                                    | 86.7 ms: 1.01x faster                                                   |
| xml_etree_iterparse  | 107 ms                                                     | 107 ms: 1.01x faster                                                    |
| unpickle             | 15.1 us                                                    | 15.0 us: 1.01x faster                                                   |
| tomli_loads          | 2.12 sec                                                   | 2.14 sec: 1.01x slower                                                  |
| pickle               | 11.5 us                                                    | 11.6 us: 1.01x slower                                                   |
| pickle_list          | 5.11 us                                                    | 5.21 us: 1.02x slower                                                   |
| Geometric mean       | (ref)                                                      | 1.01x faster                                                            |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240426-linux-x86_64-faster%2dcpython-tier_2_call-3.13.0a6+-65aa34a |
|------------------------|:----------------------------------------------------------:|:-----------------------------------------------------------------------:|
| python_startup         | 10.8 ms                                                    | 10.5 ms: 1.02x faster                                                   |
| python_startup_no_site | 7.11 ms                                                    | 7.11 ms: 1.00x slower                                                   |
| Geometric mean         | (ref)                                                      | 1.01x faster                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240426-linux-x86_64-faster%2dcpython-tier_2_call-3.13.0a6+-65aa34a |
|-----------------|:----------------------------------------------------------:|:-----------------------------------------------------------------------:|
| mako            | 11.2 ms                                                    | 10.9 ms: 1.03x faster                                                   |
| genshi_text     | 23.7 ms                                                    | 23.2 ms: 1.02x faster                                                   |
| django_template | 34.8 ms                                                    | 34.4 ms: 1.01x faster                                                   |
| genshi_xml      | 51.6 ms                                                    | 51.1 ms: 1.01x faster                                                   |
| Geometric mean  | (ref)                                                      | 1.02x faster                                                            |

All benchmarks:
===============

| Benchmark                  | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240426-linux-x86_64-faster%2dcpython-tier_2_call-3.13.0a6+-65aa34a |
|----------------------------|:----------------------------------------------------------:|:-----------------------------------------------------------------------:|
| gc_traversal               | 3.98 ms                                                    | 3.55 ms: 1.12x faster                                                   |
| logging_silent             | 105 ns                                                     | 96.3 ns: 1.09x faster                                                   |
| richards                   | 50.9 ms                                                    | 47.0 ms: 1.08x faster                                                   |
| richards_super             | 57.4 ms                                                    | 53.2 ms: 1.08x faster                                                   |
| scimark_fft                | 392 ms                                                     | 365 ms: 1.08x faster                                                    |
| async_tree_none            | 378 ms                                                     | 352 ms: 1.08x faster                                                    |
| json_loads                 | 28.9 us                                                    | 27.4 us: 1.05x faster                                                   |
| fannkuch                   | 402 ms                                                     | 383 ms: 1.05x faster                                                    |
| pyflate                    | 484 ms                                                     | 464 ms: 1.04x faster                                                    |
| deepcopy_reduce            | 3.35 us                                                    | 3.21 us: 1.04x faster                                                   |
| create_gc_cycles           | 1.82 ms                                                    | 1.75 ms: 1.04x faster                                                   |
| chameleon                  | 7.22 ms                                                    | 6.96 ms: 1.04x faster                                                   |
| json                       | 5.31 ms                                                    | 5.12 ms: 1.04x faster                                                   |
| deepcopy                   | 367 us                                                     | 355 us: 1.04x faster                                                    |
| scimark_lu                 | 122 ms                                                     | 118 ms: 1.03x faster                                                    |
| mako                       | 11.2 ms                                                    | 10.9 ms: 1.03x faster                                                   |
| crypto_pyaes               | 77.5 ms                                                    | 75.2 ms: 1.03x faster                                                   |
| unpickle_list              | 5.34 us                                                    | 5.19 us: 1.03x faster                                                   |
| scimark_monte_carlo        | 69.2 ms                                                    | 67.2 ms: 1.03x faster                                                   |
| sqlglot_transpile          | 1.63 ms                                                    | 1.59 ms: 1.03x faster                                                   |
| coroutines                 | 23.2 ms                                                    | 22.6 ms: 1.03x faster                                                   |
| scimark_sor                | 127 ms                                                     | 124 ms: 1.03x faster                                                    |
| html5lib                   | 67.2 ms                                                    | 65.6 ms: 1.03x faster                                                   |
| pprint_pformat             | 1.56 sec                                                   | 1.52 sec: 1.02x faster                                                  |
| 2to3                       | 274 ms                                                     | 267 ms: 1.02x faster                                                    |
| hexiom                     | 6.30 ms                                                    | 6.15 ms: 1.02x faster                                                   |
| unpickle_pure_python       | 218 us                                                     | 213 us: 1.02x faster                                                    |
| pprint_safe_repr           | 758 ms                                                     | 742 ms: 1.02x faster                                                    |
| sympy_str                  | 282 ms                                                     | 276 ms: 1.02x faster                                                    |
| sqlglot_parse              | 1.32 ms                                                    | 1.29 ms: 1.02x faster                                                   |
| pickle_pure_python         | 305 us                                                     | 299 us: 1.02x faster                                                    |
| python_startup             | 10.8 ms                                                    | 10.5 ms: 1.02x faster                                                   |
| async_tree_none_tg         | 336 ms                                                     | 330 ms: 1.02x faster                                                    |
| genshi_text                | 23.7 ms                                                    | 23.2 ms: 1.02x faster                                                   |
| scimark_sparse_mat_mult    | 5.27 ms                                                    | 5.17 ms: 1.02x faster                                                   |
| regex_compile              | 137 ms                                                     | 134 ms: 1.02x faster                                                    |
| go                         | 145 ms                                                     | 142 ms: 1.02x faster                                                    |
| dulwich_log                | 67.2 ms                                                    | 66.0 ms: 1.02x faster                                                   |
| chaos                      | 61.3 ms                                                    | 60.3 ms: 1.02x faster                                                   |
| xml_etree_process          | 61.2 ms                                                    | 60.2 ms: 1.02x faster                                                   |
| xml_etree_parse            | 162 ms                                                     | 159 ms: 1.02x faster                                                    |
| deepcopy_memo              | 39.7 us                                                    | 39.1 us: 1.02x faster                                                   |
| sqlglot_optimize           | 55.5 ms                                                    | 54.7 ms: 1.02x faster                                                   |
| sympy_integrate            | 20.5 ms                                                    | 20.2 ms: 1.01x faster                                                   |
| json_dumps                 | 10.7 ms                                                    | 10.6 ms: 1.01x faster                                                   |
| sqlite_synth               | 2.99 us                                                    | 2.95 us: 1.01x faster                                                   |
| sqlglot_normalize          | 110 ms                                                     | 109 ms: 1.01x faster                                                    |
| sympy_expand               | 473 ms                                                     | 467 ms: 1.01x faster                                                    |
| django_template            | 34.8 ms                                                    | 34.4 ms: 1.01x faster                                                   |
| pickle_dict                | 34.8 us                                                    | 34.4 us: 1.01x faster                                                   |
| docutils                   | 2.83 sec                                                   | 2.80 sec: 1.01x faster                                                  |
| deltablue                  | 3.25 ms                                                    | 3.22 ms: 1.01x faster                                                   |
| typing_runtime_protocols   | 165 us                                                     | 163 us: 1.01x faster                                                    |
| nbody                      | 88.3 ms                                                    | 87.4 ms: 1.01x faster                                                   |
| genshi_xml                 | 51.6 ms                                                    | 51.1 ms: 1.01x faster                                                   |
| aiohttp                    | 1.18 ms                                                    | 1.17 ms: 1.01x faster                                                   |
| thrift                     | 823 us                                                     | 816 us: 1.01x faster                                                    |
| gunicorn                   | 1.28 ms                                                    | 1.27 ms: 1.01x faster                                                   |
| xml_etree_generate         | 87.4 ms                                                    | 86.7 ms: 1.01x faster                                                   |
| xml_etree_iterparse        | 107 ms                                                     | 107 ms: 1.01x faster                                                    |
| unpickle                   | 15.1 us                                                    | 15.0 us: 1.01x faster                                                   |
| sympy_sum                  | 156 ms                                                     | 155 ms: 1.01x faster                                                    |
| logging_format             | 6.47 us                                                    | 6.42 us: 1.01x faster                                                   |
| bench_thread_pool          | 834 us                                                     | 829 us: 1.01x faster                                                    |
| asyncio_websockets         | 567 ms                                                     | 563 ms: 1.01x faster                                                    |
| asyncio_tcp                | 508 ms                                                     | 506 ms: 1.00x faster                                                    |
| async_generators           | 442 ms                                                     | 440 ms: 1.00x faster                                                    |
| tornado_http               | 94.6 ms                                                    | 94.4 ms: 1.00x faster                                                   |
| asyncio_tcp_ssl            | 1.84 sec                                                   | 1.84 sec: 1.00x faster                                                  |
| python_startup_no_site     | 7.11 ms                                                    | 7.11 ms: 1.00x slower                                                   |
| mdp                        | 2.79 sec                                                   | 2.79 sec: 1.00x slower                                                  |
| generators                 | 29.6 ms                                                    | 29.8 ms: 1.01x slower                                                   |
| telco                      | 8.41 ms                                                    | 8.49 ms: 1.01x slower                                                   |
| tomli_loads                | 2.12 sec                                                   | 2.14 sec: 1.01x slower                                                  |
| pidigits                   | 191 ms                                                     | 194 ms: 1.01x slower                                                    |
| pickle                     | 11.5 us                                                    | 11.6 us: 1.01x slower                                                   |
| pathlib                    | 17.3 ms                                                    | 17.6 ms: 1.01x slower                                                   |
| logging_simple             | 5.74 us                                                    | 5.83 us: 1.02x slower                                                   |
| comprehensions             | 16.6 us                                                    | 16.9 us: 1.02x slower                                                   |
| pickle_list                | 5.11 us                                                    | 5.21 us: 1.02x slower                                                   |
| pycparser                  | 1.16 sec                                                   | 1.20 sec: 1.03x slower                                                  |
| async_tree_cpu_io_mixed_tg | 587 ms                                                     | 609 ms: 1.04x slower                                                    |
| regex_effbot               | 3.67 ms                                                    | 3.85 ms: 1.05x slower                                                   |
| regex_v8                   | 25.1 ms                                                    | 26.3 ms: 1.05x slower                                                   |
| regex_dna                  | 221 ms                                                     | 232 ms: 1.05x slower                                                    |
| coverage                   | 93.1 ms                                                    | 98.6 ms: 1.06x slower                                                   |
| Geometric mean             | (ref)                                                      | 1.01x faster                                                            |

Benchmark hidden because not significant (15): async_tree_io, async_tree_memoization_tg, dask, mypy2, djangocms, spectral_norm, float, async_tree_io_tg, bench_mp_pool, meteor_contest, raytrace, pylint, nqueens, async_tree_memoization, async_tree_cpu_io_mixed
Ignored benchmarks (2) of results/bm-20240605-3.13.0b2-3a83b17/bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17.json: bpe_tokeniser, flaskblogging

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 0.98x