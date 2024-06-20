# Results vs. 3.13.0b2

- fork: gvanrossum
- ref: tier2_flag
- machine: linux-x86_64
- commit hash: 8cb71dd
- commit date: 2024-04-26
- overall geometric mean: 1.02x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.00x faster
- Memory change: 0.98x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240426-linux-x86_64-gvanrossum-tier2_flag-3.13.0a6+-8cb71dd |
|----------------|:----------------------------------------------------------:|:----------------------------------------------------------------:|
| 2to3           | 274 ms                                                     | 267 ms: 1.03x faster                                             |
| chameleon      | 7.22 ms                                                    | 6.96 ms: 1.04x faster                                            |
| html5lib       | 67.2 ms                                                    | 66.8 ms: 1.01x faster                                            |
| tornado_http   | 94.6 ms                                                    | 94.2 ms: 1.01x faster                                            |
| Geometric mean | (ref)                                                      | 1.02x faster                                                     |

Benchmark hidden because not significant (1): docutils

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240426-linux-x86_64-gvanrossum-tier2_flag-3.13.0a6+-8cb71dd |
|----------------------------|:----------------------------------------------------------:|:----------------------------------------------------------------:|
| async_tree_none            | 378 ms                                                     | 353 ms: 1.07x faster                                             |
| async_tree_cpu_io_mixed_tg | 587 ms                                                     | 603 ms: 1.03x slower                                             |
| Geometric mean             | (ref)                                                      | 1.01x faster                                                     |

Benchmark hidden because not significant (6): async_tree_io, async_tree_io_tg, async_tree_memoization_tg, async_tree_memoization, async_tree_none_tg, async_tree_cpu_io_mixed

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240426-linux-x86_64-gvanrossum-tier2_flag-3.13.0a6+-8cb71dd |
|----------------|:----------------------------------------------------------:|:----------------------------------------------------------------:|
| nbody          | 88.3 ms                                                    | 85.7 ms: 1.03x faster                                            |
| float          | 78.9 ms                                                    | 77.5 ms: 1.02x faster                                            |
| pidigits       | 191 ms                                                     | 193 ms: 1.01x slower                                             |
| Geometric mean | (ref)                                                      | 1.01x faster                                                     |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240426-linux-x86_64-gvanrossum-tier2_flag-3.13.0a6+-8cb71dd |
|----------------|:----------------------------------------------------------:|:----------------------------------------------------------------:|
| regex_compile  | 137 ms                                                     | 132 ms: 1.04x faster                                             |
| regex_effbot   | 3.67 ms                                                    | 3.74 ms: 1.02x slower                                            |
| regex_dna      | 221 ms                                                     | 226 ms: 1.02x slower                                             |
| regex_v8       | 25.1 ms                                                    | 25.7 ms: 1.02x slower                                            |
| Geometric mean | (ref)                                                      | 1.01x slower                                                     |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240426-linux-x86_64-gvanrossum-tier2_flag-3.13.0a6+-8cb71dd |
|----------------------|:----------------------------------------------------------:|:----------------------------------------------------------------:|
| json_loads           | 28.9 us                                                    | 27.8 us: 1.04x faster                                            |
| unpickle_list        | 5.34 us                                                    | 5.23 us: 1.02x faster                                            |
| unpickle_pure_python | 218 us                                                     | 214 us: 1.02x faster                                             |
| json_dumps           | 10.7 ms                                                    | 10.6 ms: 1.01x faster                                            |
| xml_etree_process    | 61.2 ms                                                    | 60.6 ms: 1.01x faster                                            |
| pickle_dict          | 34.8 us                                                    | 34.7 us: 1.00x faster                                            |
| tomli_loads          | 2.12 sec                                                   | 2.16 sec: 1.02x slower                                           |
| pickle               | 11.5 us                                                    | 11.8 us: 1.03x slower                                            |
| unpickle             | 15.1 us                                                    | 16.1 us: 1.07x slower                                            |
| Geometric mean       | (ref)                                                      | 1.00x faster                                                     |

Benchmark hidden because not significant (5): xml_etree_parse, xml_etree_iterparse, pickle_pure_python, xml_etree_generate, pickle_list

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240426-linux-x86_64-gvanrossum-tier2_flag-3.13.0a6+-8cb71dd |
|------------------------|:----------------------------------------------------------:|:----------------------------------------------------------------:|
| python_startup         | 10.8 ms                                                    | 10.5 ms: 1.02x faster                                            |
| python_startup_no_site | 7.11 ms                                                    | 7.09 ms: 1.00x faster                                            |
| Geometric mean         | (ref)                                                      | 1.01x faster                                                     |

Benchmarks with tag 'template':
===============================

| Benchmark      | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240426-linux-x86_64-gvanrossum-tier2_flag-3.13.0a6+-8cb71dd |
|----------------|:----------------------------------------------------------:|:----------------------------------------------------------------:|
| mako           | 11.2 ms                                                    | 10.7 ms: 1.05x faster                                            |
| genshi_text    | 23.7 ms                                                    | 23.2 ms: 1.02x faster                                            |
| Geometric mean | (ref)                                                      | 1.02x faster                                                     |

Benchmark hidden because not significant (2): genshi_xml, django_template

All benchmarks:
===============

| Benchmark                  | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240426-linux-x86_64-gvanrossum-tier2_flag-3.13.0a6+-8cb71dd |
|----------------------------|:----------------------------------------------------------:|:----------------------------------------------------------------:|
| richards                   | 50.9 ms                                                    | 46.8 ms: 1.09x faster                                            |
| scimark_fft                | 392 ms                                                     | 362 ms: 1.08x faster                                             |
| deepcopy_memo              | 39.7 us                                                    | 36.8 us: 1.08x faster                                            |
| scimark_lu                 | 122 ms                                                     | 113 ms: 1.08x faster                                             |
| async_tree_none            | 378 ms                                                     | 353 ms: 1.07x faster                                             |
| scimark_sor                | 127 ms                                                     | 119 ms: 1.07x faster                                             |
| richards_super             | 57.4 ms                                                    | 53.6 ms: 1.07x faster                                            |
| pyflate                    | 484 ms                                                     | 453 ms: 1.07x faster                                             |
| hexiom                     | 6.30 ms                                                    | 5.95 ms: 1.06x faster                                            |
| deepcopy_reduce            | 3.35 us                                                    | 3.19 us: 1.05x faster                                            |
| logging_silent             | 105 ns                                                     | 99.7 ns: 1.05x faster                                            |
| mako                       | 11.2 ms                                                    | 10.7 ms: 1.05x faster                                            |
| deepcopy                   | 367 us                                                     | 350 us: 1.05x faster                                             |
| spectral_norm              | 116 ms                                                     | 111 ms: 1.05x faster                                             |
| scimark_sparse_mat_mult    | 5.27 ms                                                    | 5.06 ms: 1.04x faster                                            |
| chaos                      | 61.3 ms                                                    | 59.1 ms: 1.04x faster                                            |
| json_loads                 | 28.9 us                                                    | 27.8 us: 1.04x faster                                            |
| sqlglot_transpile          | 1.63 ms                                                    | 1.58 ms: 1.04x faster                                            |
| chameleon                  | 7.22 ms                                                    | 6.96 ms: 1.04x faster                                            |
| regex_compile              | 137 ms                                                     | 132 ms: 1.04x faster                                             |
| crypto_pyaes               | 77.5 ms                                                    | 74.7 ms: 1.04x faster                                            |
| sqlglot_parse              | 1.32 ms                                                    | 1.28 ms: 1.03x faster                                            |
| json                       | 5.31 ms                                                    | 5.13 ms: 1.03x faster                                            |
| create_gc_cycles           | 1.82 ms                                                    | 1.76 ms: 1.03x faster                                            |
| nqueens                    | 81.4 ms                                                    | 78.8 ms: 1.03x faster                                            |
| fannkuch                   | 402 ms                                                     | 389 ms: 1.03x faster                                             |
| go                         | 145 ms                                                     | 140 ms: 1.03x faster                                             |
| pprint_pformat             | 1.56 sec                                                   | 1.51 sec: 1.03x faster                                           |
| nbody                      | 88.3 ms                                                    | 85.7 ms: 1.03x faster                                            |
| raytrace                   | 267 ms                                                     | 259 ms: 1.03x faster                                             |
| deltablue                  | 3.25 ms                                                    | 3.16 ms: 1.03x faster                                            |
| sqlite_synth               | 2.99 us                                                    | 2.90 us: 1.03x faster                                            |
| pprint_safe_repr           | 758 ms                                                     | 738 ms: 1.03x faster                                             |
| 2to3                       | 274 ms                                                     | 267 ms: 1.03x faster                                             |
| mdp                        | 2.79 sec                                                   | 2.71 sec: 1.03x faster                                           |
| python_startup             | 10.8 ms                                                    | 10.5 ms: 1.02x faster                                            |
| unpickle_list              | 5.34 us                                                    | 5.23 us: 1.02x faster                                            |
| logging_format             | 6.47 us                                                    | 6.33 us: 1.02x faster                                            |
| genshi_text                | 23.7 ms                                                    | 23.2 ms: 1.02x faster                                            |
| unpickle_pure_python       | 218 us                                                     | 214 us: 1.02x faster                                             |
| sympy_str                  | 282 ms                                                     | 277 ms: 1.02x faster                                             |
| scimark_monte_carlo        | 69.2 ms                                                    | 67.9 ms: 1.02x faster                                            |
| comprehensions             | 16.6 us                                                    | 16.3 us: 1.02x faster                                            |
| float                      | 78.9 ms                                                    | 77.5 ms: 1.02x faster                                            |
| bench_thread_pool          | 834 us                                                     | 820 us: 1.02x faster                                             |
| sqlglot_optimize           | 55.5 ms                                                    | 54.6 ms: 1.02x faster                                            |
| generators                 | 29.6 ms                                                    | 29.2 ms: 1.02x faster                                            |
| json_dumps                 | 10.7 ms                                                    | 10.6 ms: 1.01x faster                                            |
| meteor_contest             | 110 ms                                                     | 108 ms: 1.01x faster                                             |
| sympy_integrate            | 20.5 ms                                                    | 20.3 ms: 1.01x faster                                            |
| xml_etree_process          | 61.2 ms                                                    | 60.6 ms: 1.01x faster                                            |
| sqlglot_normalize          | 110 ms                                                     | 109 ms: 1.01x faster                                             |
| logging_simple             | 5.74 us                                                    | 5.70 us: 1.01x faster                                            |
| typing_runtime_protocols   | 165 us                                                     | 163 us: 1.01x faster                                             |
| sympy_expand               | 473 ms                                                     | 469 ms: 1.01x faster                                             |
| aiohttp                    | 1.18 ms                                                    | 1.17 ms: 1.01x faster                                            |
| dulwich_log                | 67.2 ms                                                    | 66.7 ms: 1.01x faster                                            |
| html5lib                   | 67.2 ms                                                    | 66.8 ms: 1.01x faster                                            |
| sympy_sum                  | 156 ms                                                     | 155 ms: 1.01x faster                                             |
| tornado_http               | 94.6 ms                                                    | 94.2 ms: 1.01x faster                                            |
| asyncio_websockets         | 567 ms                                                     | 564 ms: 1.00x faster                                             |
| python_startup_no_site     | 7.11 ms                                                    | 7.09 ms: 1.00x faster                                            |
| pickle_dict                | 34.8 us                                                    | 34.7 us: 1.00x faster                                            |
| asyncio_tcp_ssl            | 1.84 sec                                                   | 1.85 sec: 1.00x slower                                           |
| pidigits                   | 191 ms                                                     | 193 ms: 1.01x slower                                             |
| gc_traversal               | 3.98 ms                                                    | 4.02 ms: 1.01x slower                                            |
| asyncio_tcp                | 508 ms                                                     | 515 ms: 1.01x slower                                             |
| telco                      | 8.41 ms                                                    | 8.56 ms: 1.02x slower                                            |
| regex_effbot               | 3.67 ms                                                    | 3.74 ms: 1.02x slower                                            |
| pathlib                    | 17.3 ms                                                    | 17.6 ms: 1.02x slower                                            |
| tomli_loads                | 2.12 sec                                                   | 2.16 sec: 1.02x slower                                           |
| regex_dna                  | 221 ms                                                     | 226 ms: 1.02x slower                                             |
| regex_v8                   | 25.1 ms                                                    | 25.7 ms: 1.02x slower                                            |
| async_tree_cpu_io_mixed_tg | 587 ms                                                     | 603 ms: 1.03x slower                                             |
| pickle                     | 11.5 us                                                    | 11.8 us: 1.03x slower                                            |
| pycparser                  | 1.16 sec                                                   | 1.19 sec: 1.03x slower                                           |
| unpickle                   | 15.1 us                                                    | 16.1 us: 1.07x slower                                            |
| Geometric mean             | (ref)                                                      | 1.02x faster                                                     |

Benchmark hidden because not significant (24): async_tree_io, async_tree_io_tg, mypy2, xml_etree_parse, xml_etree_iterparse, gunicorn, async_tree_memoization_tg, async_tree_memoization, coverage, docutils, djangocms, thrift, genshi_xml, pickle_pure_python, async_tree_none_tg, bench_mp_pool, dask, async_tree_cpu_io_mixed, async_generators, django_template, xml_etree_generate, pylint, pickle_list, coroutines
Ignored benchmarks (2) of results/bm-20240605-3.13.0b2-3a83b17/bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17.json: bpe_tokeniser, flaskblogging

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 0.98x