# Results vs. 3.13.0b2

- fork: python
- ref: 027fa2eccf39ddccdf7b
- machine: linux-x86_64
- commit hash: 027fa2e
- commit date: 2024-04-02
- overall geometric mean: 1.00x slower
- HPT reliability: 98.74%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.06x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240402-linux-x86_64-python-027fa2eccf39ddccdf7b-3.13.0a5+-027fa2e |
|----------------|:----------------------------------------------------------:|:----------------------------------------------------------------------:|
| 2to3           | 274 ms                                                     | 277 ms: 1.01x slower                                                   |
| chameleon      | 7.22 ms                                                    | 6.86 ms: 1.05x faster                                                  |
| docutils       | 2.83 sec                                                   | 2.90 sec: 1.03x slower                                                 |
| html5lib       | 67.2 ms                                                    | 65.5 ms: 1.03x faster                                                  |
| tornado_http   | 94.6 ms                                                    | 96.1 ms: 1.02x slower                                                  |
| Geometric mean | (ref)                                                      | 1.00x faster                                                           |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240402-linux-x86_64-python-027fa2eccf39ddccdf7b-3.13.0a5+-027fa2e |
|----------------------------|:----------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_none            | 378 ms                                                     | 355 ms: 1.06x faster                                                   |
| async_tree_cpu_io_mixed_tg | 587 ms                                                     | 609 ms: 1.04x slower                                                   |
| Geometric mean             | (ref)                                                      | 1.00x faster                                                           |

Benchmark hidden because not significant (6): async_tree_memoization, async_tree_io, async_tree_memoization_tg, async_tree_none_tg, async_tree_cpu_io_mixed, async_tree_io_tg

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240402-linux-x86_64-python-027fa2eccf39ddccdf7b-3.13.0a5+-027fa2e |
|----------------|:----------------------------------------------------------:|:----------------------------------------------------------------------:|
| float          | 78.9 ms                                                    | 76.2 ms: 1.03x faster                                                  |
| nbody          | 88.3 ms                                                    | 91.7 ms: 1.04x slower                                                  |
| pidigits       | 191 ms                                                     | 202 ms: 1.05x slower                                                   |
| Geometric mean | (ref)                                                      | 1.02x slower                                                           |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240402-linux-x86_64-python-027fa2eccf39ddccdf7b-3.13.0a5+-027fa2e |
|----------------|:----------------------------------------------------------:|:----------------------------------------------------------------------:|
| regex_effbot   | 3.67 ms                                                    | 3.60 ms: 1.02x faster                                                  |
| regex_v8       | 25.1 ms                                                    | 25.0 ms: 1.01x faster                                                  |
| regex_dna      | 221 ms                                                     | 220 ms: 1.00x faster                                                   |
| regex_compile  | 137 ms                                                     | 146 ms: 1.07x slower                                                   |
| Geometric mean | (ref)                                                      | 1.01x slower                                                           |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240402-linux-x86_64-python-027fa2eccf39ddccdf7b-3.13.0a5+-027fa2e |
|----------------------|:----------------------------------------------------------:|:----------------------------------------------------------------------:|
| unpickle_list        | 5.34 us                                                    | 5.18 us: 1.03x faster                                                  |
| tomli_loads          | 2.12 sec                                                   | 2.07 sec: 1.03x faster                                                 |
| xml_etree_process    | 61.2 ms                                                    | 59.7 ms: 1.03x faster                                                  |
| pickle_dict          | 34.8 us                                                    | 34.0 us: 1.02x faster                                                  |
| unpickle             | 15.1 us                                                    | 14.8 us: 1.02x faster                                                  |
| pickle_list          | 5.11 us                                                    | 5.02 us: 1.02x faster                                                  |
| xml_etree_parse      | 162 ms                                                     | 159 ms: 1.02x faster                                                   |
| xml_etree_generate   | 87.4 ms                                                    | 86.7 ms: 1.01x faster                                                  |
| xml_etree_iterparse  | 107 ms                                                     | 107 ms: 1.01x faster                                                   |
| pickle               | 11.5 us                                                    | 12.0 us: 1.05x slower                                                  |
| unpickle_pure_python | 218 us                                                     | 236 us: 1.08x slower                                                   |
| Geometric mean       | (ref)                                                      | 1.00x faster                                                           |

Benchmark hidden because not significant (3): json_loads, json_dumps, pickle_pure_python

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240402-linux-x86_64-python-027fa2eccf39ddccdf7b-3.13.0a5+-027fa2e |
|------------------------|:----------------------------------------------------------:|:----------------------------------------------------------------------:|
| python_startup         | 10.8 ms                                                    | 11.0 ms: 1.03x slower                                                  |
| python_startup_no_site | 7.11 ms                                                    | 9.49 ms: 1.33x slower                                                  |
| Geometric mean         | (ref)                                                      | 1.17x slower                                                           |

Benchmarks with tag 'template':
===============================

| Benchmark      | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240402-linux-x86_64-python-027fa2eccf39ddccdf7b-3.13.0a5+-027fa2e |
|----------------|:----------------------------------------------------------:|:----------------------------------------------------------------------:|
| mako           | 11.2 ms                                                    | 10.9 ms: 1.03x faster                                                  |
| genshi_text    | 23.7 ms                                                    | 24.6 ms: 1.04x slower                                                  |
| genshi_xml     | 51.6 ms                                                    | 55.0 ms: 1.07x slower                                                  |
| Geometric mean | (ref)                                                      | 1.02x slower                                                           |

All benchmarks:
===============

| Benchmark                  | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240402-linux-x86_64-python-027fa2eccf39ddccdf7b-3.13.0a5+-027fa2e |
|----------------------------|:----------------------------------------------------------:|:----------------------------------------------------------------------:|
| typing_runtime_protocols   | 165 us                                                     | 111 us: 1.48x faster                                                   |
| scimark_fft                | 392 ms                                                     | 346 ms: 1.14x faster                                                   |
| richards                   | 50.9 ms                                                    | 45.9 ms: 1.11x faster                                                  |
| richards_super             | 57.4 ms                                                    | 52.2 ms: 1.10x faster                                                  |
| logging_silent             | 105 ns                                                     | 97.9 ns: 1.07x faster                                                  |
| pylint                     | 317 ms                                                     | 298 ms: 1.07x faster                                                   |
| async_tree_none            | 378 ms                                                     | 355 ms: 1.06x faster                                                   |
| mdp                        | 2.79 sec                                                   | 2.63 sec: 1.06x faster                                                 |
| chameleon                  | 7.22 ms                                                    | 6.86 ms: 1.05x faster                                                  |
| scimark_sparse_mat_mult    | 5.27 ms                                                    | 5.02 ms: 1.05x faster                                                  |
| gc_traversal               | 3.98 ms                                                    | 3.79 ms: 1.05x faster                                                  |
| sqlite_synth               | 2.99 us                                                    | 2.85 us: 1.05x faster                                                  |
| coroutines                 | 23.2 ms                                                    | 22.2 ms: 1.04x faster                                                  |
| deepcopy_reduce            | 3.35 us                                                    | 3.23 us: 1.04x faster                                                  |
| float                      | 78.9 ms                                                    | 76.2 ms: 1.03x faster                                                  |
| crypto_pyaes               | 77.5 ms                                                    | 74.9 ms: 1.03x faster                                                  |
| pprint_safe_repr           | 758 ms                                                     | 733 ms: 1.03x faster                                                   |
| unpickle_list              | 5.34 us                                                    | 5.18 us: 1.03x faster                                                  |
| pyflate                    | 484 ms                                                     | 469 ms: 1.03x faster                                                   |
| create_gc_cycles           | 1.82 ms                                                    | 1.76 ms: 1.03x faster                                                  |
| mako                       | 11.2 ms                                                    | 10.9 ms: 1.03x faster                                                  |
| deepcopy_memo              | 39.7 us                                                    | 38.5 us: 1.03x faster                                                  |
| pprint_pformat             | 1.56 sec                                                   | 1.51 sec: 1.03x faster                                                 |
| html5lib                   | 67.2 ms                                                    | 65.5 ms: 1.03x faster                                                  |
| tomli_loads                | 2.12 sec                                                   | 2.07 sec: 1.03x faster                                                 |
| xml_etree_process          | 61.2 ms                                                    | 59.7 ms: 1.03x faster                                                  |
| pickle_dict                | 34.8 us                                                    | 34.0 us: 1.02x faster                                                  |
| unpickle                   | 15.1 us                                                    | 14.8 us: 1.02x faster                                                  |
| regex_effbot               | 3.67 ms                                                    | 3.60 ms: 1.02x faster                                                  |
| pickle_list                | 5.11 us                                                    | 5.02 us: 1.02x faster                                                  |
| xml_etree_parse            | 162 ms                                                     | 159 ms: 1.02x faster                                                   |
| spectral_norm              | 116 ms                                                     | 115 ms: 1.01x faster                                                   |
| fannkuch                   | 402 ms                                                     | 398 ms: 1.01x faster                                                   |
| xml_etree_generate         | 87.4 ms                                                    | 86.7 ms: 1.01x faster                                                  |
| xml_etree_iterparse        | 107 ms                                                     | 107 ms: 1.01x faster                                                   |
| deepcopy                   | 367 us                                                     | 364 us: 1.01x faster                                                   |
| regex_v8                   | 25.1 ms                                                    | 25.0 ms: 1.01x faster                                                  |
| asyncio_websockets         | 567 ms                                                     | 564 ms: 1.01x faster                                                   |
| regex_dna                  | 221 ms                                                     | 220 ms: 1.00x faster                                                   |
| sqlglot_transpile          | 1.63 ms                                                    | 1.64 ms: 1.00x slower                                                  |
| asyncio_tcp_ssl            | 1.84 sec                                                   | 1.86 sec: 1.01x slower                                                 |
| meteor_contest             | 110 ms                                                     | 111 ms: 1.01x slower                                                   |
| 2to3                       | 274 ms                                                     | 277 ms: 1.01x slower                                                   |
| telco                      | 8.41 ms                                                    | 8.51 ms: 1.01x slower                                                  |
| chaos                      | 61.3 ms                                                    | 62.1 ms: 1.01x slower                                                  |
| tornado_http               | 94.6 ms                                                    | 96.1 ms: 1.02x slower                                                  |
| dask                       | 369 ms                                                     | 376 ms: 1.02x slower                                                   |
| gunicorn                   | 1.28 ms                                                    | 1.30 ms: 1.02x slower                                                  |
| logging_format             | 6.47 us                                                    | 6.61 us: 1.02x slower                                                  |
| asyncio_tcp                | 508 ms                                                     | 520 ms: 1.02x slower                                                   |
| json                       | 5.31 ms                                                    | 5.44 ms: 1.03x slower                                                  |
| python_startup             | 10.8 ms                                                    | 11.0 ms: 1.03x slower                                                  |
| docutils                   | 2.83 sec                                                   | 2.90 sec: 1.03x slower                                                 |
| aiohttp                    | 1.18 ms                                                    | 1.21 ms: 1.03x slower                                                  |
| bench_thread_pool          | 834 us                                                     | 859 us: 1.03x slower                                                   |
| sqlglot_normalize          | 110 ms                                                     | 114 ms: 1.04x slower                                                   |
| async_tree_cpu_io_mixed_tg | 587 ms                                                     | 609 ms: 1.04x slower                                                   |
| genshi_text                | 23.7 ms                                                    | 24.6 ms: 1.04x slower                                                  |
| nbody                      | 88.3 ms                                                    | 91.7 ms: 1.04x slower                                                  |
| async_generators           | 442 ms                                                     | 460 ms: 1.04x slower                                                   |
| logging_simple             | 5.74 us                                                    | 5.98 us: 1.04x slower                                                  |
| sympy_str                  | 282 ms                                                     | 294 ms: 1.04x slower                                                   |
| sqlglot_optimize           | 55.5 ms                                                    | 58.0 ms: 1.04x slower                                                  |
| sympy_expand               | 473 ms                                                     | 494 ms: 1.05x slower                                                   |
| pickle                     | 11.5 us                                                    | 12.0 us: 1.05x slower                                                  |
| raytrace                   | 267 ms                                                     | 280 ms: 1.05x slower                                                   |
| deltablue                  | 3.25 ms                                                    | 3.42 ms: 1.05x slower                                                  |
| coverage                   | 93.1 ms                                                    | 98.1 ms: 1.05x slower                                                  |
| pidigits                   | 191 ms                                                     | 202 ms: 1.05x slower                                                   |
| go                         | 145 ms                                                     | 153 ms: 1.06x slower                                                   |
| dulwich_log                | 67.2 ms                                                    | 71.2 ms: 1.06x slower                                                  |
| mypy2                      | 742 ms                                                     | 786 ms: 1.06x slower                                                   |
| scimark_sor                | 127 ms                                                     | 135 ms: 1.06x slower                                                   |
| genshi_xml                 | 51.6 ms                                                    | 55.0 ms: 1.07x slower                                                  |
| regex_compile              | 137 ms                                                     | 146 ms: 1.07x slower                                                   |
| sympy_integrate            | 20.5 ms                                                    | 22.0 ms: 1.07x slower                                                  |
| sympy_sum                  | 156 ms                                                     | 167 ms: 1.07x slower                                                   |
| comprehensions             | 16.6 us                                                    | 17.9 us: 1.08x slower                                                  |
| unpickle_pure_python       | 218 us                                                     | 236 us: 1.08x slower                                                   |
| scimark_lu                 | 122 ms                                                     | 132 ms: 1.09x slower                                                   |
| pathlib                    | 17.3 ms                                                    | 19.1 ms: 1.10x slower                                                  |
| nqueens                    | 81.4 ms                                                    | 91.4 ms: 1.12x slower                                                  |
| hexiom                     | 6.30 ms                                                    | 7.08 ms: 1.13x slower                                                  |
| python_startup_no_site     | 7.11 ms                                                    | 9.49 ms: 1.33x slower                                                  |
| Geometric mean             | (ref)                                                      | 1.00x slower                                                           |

Benchmark hidden because not significant (15): async_tree_memoization, async_tree_io, json_loads, json_dumps, pycparser, async_tree_memoization_tg, pickle_pure_python, generators, scimark_monte_carlo, sqlglot_parse, thrift, bench_mp_pool, async_tree_none_tg, async_tree_cpu_io_mixed, async_tree_io_tg
Ignored benchmarks (4) of results/bm-20240605-3.13.0b2-3a83b17/bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17.json: bpe_tokeniser, django_template, djangocms, flaskblogging

# HPT report

- Reliability score: 98.74% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.06x