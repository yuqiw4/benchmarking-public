# Results vs. 3.13.0b2

- fork: python
- ref: 15fbd53ba96be4b6a5ab
- machine: linux-x86_64
- commit hash: 15fbd53
- commit date: 2024-04-20
- overall geometric mean: 1.01x faster
- HPT reliability: 99.97%
- HPT 99th percentile: 1.00x faster
- Memory change: 0.98x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240420-linux-x86_64-python-15fbd53ba96be4b6a5ab-3.13.0a6+-15fbd53 |
|----------------|:----------------------------------------------------------:|:----------------------------------------------------------------------:|
| 2to3           | 274 ms                                                     | 268 ms: 1.02x faster                                                   |
| chameleon      | 7.22 ms                                                    | 7.04 ms: 1.03x faster                                                  |
| docutils       | 2.83 sec                                                   | 2.80 sec: 1.01x faster                                                 |
| tornado_http   | 94.6 ms                                                    | 94.2 ms: 1.00x faster                                                  |
| Geometric mean | (ref)                                                      | 1.01x faster                                                           |

Benchmark hidden because not significant (1): html5lib

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240420-linux-x86_64-python-15fbd53ba96be4b6a5ab-3.13.0a6+-15fbd53 |
|----------------------------|:----------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_none            | 378 ms                                                     | 352 ms: 1.08x faster                                                   |
| async_tree_cpu_io_mixed_tg | 587 ms                                                     | 605 ms: 1.03x slower                                                   |
| Geometric mean             | (ref)                                                      | 1.01x faster                                                           |

Benchmark hidden because not significant (6): async_tree_io, async_tree_memoization, async_tree_memoization_tg, async_tree_cpu_io_mixed, async_tree_none_tg, async_tree_io_tg

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240420-linux-x86_64-python-15fbd53ba96be4b6a5ab-3.13.0a6+-15fbd53 |
|----------------|:----------------------------------------------------------:|:----------------------------------------------------------------------:|
| pidigits       | 191 ms                                                     | 193 ms: 1.01x slower                                                   |
| Geometric mean | (ref)                                                      | 1.00x slower                                                           |

Benchmark hidden because not significant (2): float, nbody

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240420-linux-x86_64-python-15fbd53ba96be4b6a5ab-3.13.0a6+-15fbd53 |
|----------------|:----------------------------------------------------------:|:----------------------------------------------------------------------:|
| regex_v8       | 25.1 ms                                                    | 24.6 ms: 1.02x faster                                                  |
| regex_compile  | 137 ms                                                     | 135 ms: 1.01x faster                                                   |
| regex_effbot   | 3.67 ms                                                    | 3.74 ms: 1.02x slower                                                  |
| Geometric mean | (ref)                                                      | 1.00x faster                                                           |

Benchmark hidden because not significant (1): regex_dna

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240420-linux-x86_64-python-15fbd53ba96be4b6a5ab-3.13.0a6+-15fbd53 |
|----------------------|:----------------------------------------------------------:|:----------------------------------------------------------------------:|
| json_loads           | 28.9 us                                                    | 27.6 us: 1.05x faster                                                  |
| xml_etree_parse      | 162 ms                                                     | 157 ms: 1.03x faster                                                   |
| unpickle_pure_python | 218 us                                                     | 213 us: 1.02x faster                                                   |
| json_dumps           | 10.7 ms                                                    | 10.6 ms: 1.02x faster                                                  |
| pickle_pure_python   | 305 us                                                     | 302 us: 1.01x faster                                                   |
| xml_etree_process    | 61.2 ms                                                    | 60.6 ms: 1.01x faster                                                  |
| xml_etree_generate   | 87.4 ms                                                    | 87.1 ms: 1.00x faster                                                  |
| pickle_list          | 5.11 us                                                    | 5.16 us: 1.01x slower                                                  |
| pickle               | 11.5 us                                                    | 11.6 us: 1.01x slower                                                  |
| unpickle_list        | 5.34 us                                                    | 5.46 us: 1.02x slower                                                  |
| pickle_dict          | 34.8 us                                                    | 35.6 us: 1.02x slower                                                  |
| tomli_loads          | 2.12 sec                                                   | 2.18 sec: 1.03x slower                                                 |
| Geometric mean       | (ref)                                                      | 1.00x faster                                                           |

Benchmark hidden because not significant (2): xml_etree_iterparse, unpickle

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240420-linux-x86_64-python-15fbd53ba96be4b6a5ab-3.13.0a6+-15fbd53 |
|------------------------|:----------------------------------------------------------:|:----------------------------------------------------------------------:|
| python_startup         | 10.8 ms                                                    | 10.5 ms: 1.03x faster                                                  |
| python_startup_no_site | 7.11 ms                                                    | 7.08 ms: 1.00x faster                                                  |
| Geometric mean         | (ref)                                                      | 1.01x faster                                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240420-linux-x86_64-python-15fbd53ba96be4b6a5ab-3.13.0a6+-15fbd53 |
|-----------------|:----------------------------------------------------------:|:----------------------------------------------------------------------:|
| mako            | 11.2 ms                                                    | 10.7 ms: 1.05x faster                                                  |
| django_template | 34.8 ms                                                    | 35.0 ms: 1.01x slower                                                  |
| genshi_text     | 23.7 ms                                                    | 24.3 ms: 1.03x slower                                                  |
| genshi_xml      | 51.6 ms                                                    | 52.9 ms: 1.03x slower                                                  |
| Geometric mean  | (ref)                                                      | 1.00x slower                                                           |

All benchmarks:
===============

| Benchmark                  | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240420-linux-x86_64-python-15fbd53ba96be4b6a5ab-3.13.0a6+-15fbd53 |
|----------------------------|:----------------------------------------------------------:|:----------------------------------------------------------------------:|
| typing_runtime_protocols   | 165 us                                                     | 117 us: 1.41x faster                                                   |
| richards                   | 50.9 ms                                                    | 47.0 ms: 1.08x faster                                                  |
| richards_super             | 57.4 ms                                                    | 53.0 ms: 1.08x faster                                                  |
| async_tree_none            | 378 ms                                                     | 352 ms: 1.08x faster                                                   |
| scimark_lu                 | 122 ms                                                     | 114 ms: 1.07x faster                                                   |
| deepcopy_memo              | 39.7 us                                                    | 37.4 us: 1.06x faster                                                  |
| gc_traversal               | 3.98 ms                                                    | 3.78 ms: 1.05x faster                                                  |
| mako                       | 11.2 ms                                                    | 10.7 ms: 1.05x faster                                                  |
| scimark_fft                | 392 ms                                                     | 374 ms: 1.05x faster                                                   |
| json_loads                 | 28.9 us                                                    | 27.6 us: 1.05x faster                                                  |
| logging_silent             | 105 ns                                                     | 100 ns: 1.05x faster                                                   |
| create_gc_cycles           | 1.82 ms                                                    | 1.74 ms: 1.04x faster                                                  |
| pprint_pformat             | 1.56 sec                                                   | 1.51 sec: 1.03x faster                                                 |
| spectral_norm              | 116 ms                                                     | 113 ms: 1.03x faster                                                   |
| deepcopy_reduce            | 3.35 us                                                    | 3.25 us: 1.03x faster                                                  |
| xml_etree_parse            | 162 ms                                                     | 157 ms: 1.03x faster                                                   |
| json                       | 5.31 ms                                                    | 5.15 ms: 1.03x faster                                                  |
| crypto_pyaes               | 77.5 ms                                                    | 75.4 ms: 1.03x faster                                                  |
| deepcopy                   | 367 us                                                     | 358 us: 1.03x faster                                                   |
| chameleon                  | 7.22 ms                                                    | 7.04 ms: 1.03x faster                                                  |
| pprint_safe_repr           | 758 ms                                                     | 740 ms: 1.03x faster                                                   |
| python_startup             | 10.8 ms                                                    | 10.5 ms: 1.03x faster                                                  |
| sqlglot_transpile          | 1.63 ms                                                    | 1.60 ms: 1.02x faster                                                  |
| 2to3                       | 274 ms                                                     | 268 ms: 1.02x faster                                                   |
| sqlglot_parse              | 1.32 ms                                                    | 1.29 ms: 1.02x faster                                                  |
| unpickle_pure_python       | 218 us                                                     | 213 us: 1.02x faster                                                   |
| coroutines                 | 23.2 ms                                                    | 22.7 ms: 1.02x faster                                                  |
| fannkuch                   | 402 ms                                                     | 393 ms: 1.02x faster                                                   |
| regex_v8                   | 25.1 ms                                                    | 24.6 ms: 1.02x faster                                                  |
| mdp                        | 2.79 sec                                                   | 2.73 sec: 1.02x faster                                                 |
| raytrace                   | 267 ms                                                     | 262 ms: 1.02x faster                                                   |
| nqueens                    | 81.4 ms                                                    | 79.9 ms: 1.02x faster                                                  |
| dulwich_log                | 67.2 ms                                                    | 66.0 ms: 1.02x faster                                                  |
| thrift                     | 823 us                                                     | 810 us: 1.02x faster                                                   |
| json_dumps                 | 10.7 ms                                                    | 10.6 ms: 1.02x faster                                                  |
| sqlglot_optimize           | 55.5 ms                                                    | 54.7 ms: 1.01x faster                                                  |
| sqlglot_normalize          | 110 ms                                                     | 109 ms: 1.01x faster                                                   |
| chaos                      | 61.3 ms                                                    | 60.6 ms: 1.01x faster                                                  |
| regex_compile              | 137 ms                                                     | 135 ms: 1.01x faster                                                   |
| hexiom                     | 6.30 ms                                                    | 6.23 ms: 1.01x faster                                                  |
| pickle_pure_python         | 305 us                                                     | 302 us: 1.01x faster                                                   |
| sympy_str                  | 282 ms                                                     | 279 ms: 1.01x faster                                                   |
| xml_etree_process          | 61.2 ms                                                    | 60.6 ms: 1.01x faster                                                  |
| aiohttp                    | 1.18 ms                                                    | 1.17 ms: 1.01x faster                                                  |
| docutils                   | 2.83 sec                                                   | 2.80 sec: 1.01x faster                                                 |
| sympy_integrate            | 20.5 ms                                                    | 20.3 ms: 1.01x faster                                                  |
| scimark_sparse_mat_mult    | 5.27 ms                                                    | 5.23 ms: 1.01x faster                                                  |
| sympy_expand               | 473 ms                                                     | 469 ms: 1.01x faster                                                   |
| scimark_monte_carlo        | 69.2 ms                                                    | 68.7 ms: 1.01x faster                                                  |
| gunicorn                   | 1.28 ms                                                    | 1.27 ms: 1.01x faster                                                  |
| asyncio_tcp                | 508 ms                                                     | 505 ms: 1.01x faster                                                   |
| asyncio_websockets         | 567 ms                                                     | 564 ms: 1.01x faster                                                   |
| bench_thread_pool          | 834 us                                                     | 830 us: 1.00x faster                                                   |
| tornado_http               | 94.6 ms                                                    | 94.2 ms: 1.00x faster                                                  |
| python_startup_no_site     | 7.11 ms                                                    | 7.08 ms: 1.00x faster                                                  |
| xml_etree_generate         | 87.4 ms                                                    | 87.1 ms: 1.00x faster                                                  |
| django_template            | 34.8 ms                                                    | 35.0 ms: 1.01x slower                                                  |
| sympy_sum                  | 156 ms                                                     | 157 ms: 1.01x slower                                                   |
| generators                 | 29.6 ms                                                    | 29.9 ms: 1.01x slower                                                  |
| pidigits                   | 191 ms                                                     | 193 ms: 1.01x slower                                                   |
| pickle_list                | 5.11 us                                                    | 5.16 us: 1.01x slower                                                  |
| scimark_sor                | 127 ms                                                     | 129 ms: 1.01x slower                                                   |
| pickle                     | 11.5 us                                                    | 11.6 us: 1.01x slower                                                  |
| logging_format             | 6.47 us                                                    | 6.57 us: 1.01x slower                                                  |
| regex_effbot               | 3.67 ms                                                    | 3.74 ms: 1.02x slower                                                  |
| pathlib                    | 17.3 ms                                                    | 17.7 ms: 1.02x slower                                                  |
| unpickle_list              | 5.34 us                                                    | 5.46 us: 1.02x slower                                                  |
| pickle_dict                | 34.8 us                                                    | 35.6 us: 1.02x slower                                                  |
| genshi_text                | 23.7 ms                                                    | 24.3 ms: 1.03x slower                                                  |
| genshi_xml                 | 51.6 ms                                                    | 52.9 ms: 1.03x slower                                                  |
| tomli_loads                | 2.12 sec                                                   | 2.18 sec: 1.03x slower                                                 |
| async_tree_cpu_io_mixed_tg | 587 ms                                                     | 605 ms: 1.03x slower                                                   |
| logging_simple             | 5.74 us                                                    | 5.95 us: 1.04x slower                                                  |
| telco                      | 8.41 ms                                                    | 8.74 ms: 1.04x slower                                                  |
| coverage                   | 93.1 ms                                                    | 97.5 ms: 1.05x slower                                                  |
| Geometric mean             | (ref)                                                      | 1.01x faster                                                           |

Benchmark hidden because not significant (26): async_tree_io, mypy2, pycparser, async_tree_memoization, async_tree_memoization_tg, dask, sqlite_synth, deltablue, pyflate, async_generators, float, comprehensions, asyncio_tcp_ssl, regex_dna, meteor_contest, html5lib, async_tree_cpu_io_mixed, go, xml_etree_iterparse, async_tree_none_tg, async_tree_io_tg, bench_mp_pool, pylint, nbody, djangocms, unpickle
Ignored benchmarks (2) of results/bm-20240605-3.13.0b2-3a83b17/bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17.json: bpe_tokeniser, flaskblogging

# HPT report

- Reliability score: 99.97% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 0.98x