# Results vs. 3.13.0b2

- fork: gvanrossum
- ref: disable_tier2
- machine: linux-x86_64
- commit hash: 2055e5f
- commit date: 2024-04-15
- overall geometric mean: 1.02x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.00x faster
- Memory change: 0.98x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240415-linux-x86_64-gvanrossum-disable_tier2-3.13.0a6+-2055e5f |
|----------------|:----------------------------------------------------------:|:-------------------------------------------------------------------:|
| 2to3           | 274 ms                                                     | 268 ms: 1.02x faster                                                |
| chameleon      | 7.22 ms                                                    | 6.91 ms: 1.04x faster                                               |
| docutils       | 2.83 sec                                                   | 2.79 sec: 1.01x faster                                              |
| tornado_http   | 94.6 ms                                                    | 94.3 ms: 1.00x faster                                               |
| Geometric mean | (ref)                                                      | 1.02x faster                                                        |

Benchmark hidden because not significant (1): html5lib

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240415-linux-x86_64-gvanrossum-disable_tier2-3.13.0a6+-2055e5f |
|----------------------------|:----------------------------------------------------------:|:-------------------------------------------------------------------:|
| async_tree_none            | 378 ms                                                     | 352 ms: 1.08x faster                                                |
| async_tree_cpu_io_mixed_tg | 587 ms                                                     | 603 ms: 1.03x slower                                                |
| Geometric mean             | (ref)                                                      | 1.02x faster                                                        |

Benchmark hidden because not significant (6): async_tree_io_tg, async_tree_io, async_tree_none_tg, async_tree_memoization_tg, async_tree_cpu_io_mixed, async_tree_memoization

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240415-linux-x86_64-gvanrossum-disable_tier2-3.13.0a6+-2055e5f |
|----------------|:----------------------------------------------------------:|:-------------------------------------------------------------------:|
| nbody          | 88.3 ms                                                    | 85.7 ms: 1.03x faster                                               |
| float          | 78.9 ms                                                    | 77.7 ms: 1.02x faster                                               |
| pidigits       | 191 ms                                                     | 198 ms: 1.04x slower                                                |
| Geometric mean | (ref)                                                      | 1.00x faster                                                        |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240415-linux-x86_64-gvanrossum-disable_tier2-3.13.0a6+-2055e5f |
|----------------|:----------------------------------------------------------:|:-------------------------------------------------------------------:|
| regex_compile  | 137 ms                                                     | 134 ms: 1.02x faster                                                |
| regex_dna      | 221 ms                                                     | 226 ms: 1.02x slower                                                |
| regex_v8       | 25.1 ms                                                    | 25.9 ms: 1.03x slower                                               |
| regex_effbot   | 3.67 ms                                                    | 3.82 ms: 1.04x slower                                               |
| Geometric mean | (ref)                                                      | 1.02x slower                                                        |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240415-linux-x86_64-gvanrossum-disable_tier2-3.13.0a6+-2055e5f |
|----------------------|:----------------------------------------------------------:|:-------------------------------------------------------------------:|
| unpickle_list        | 5.34 us                                                    | 5.07 us: 1.05x faster                                               |
| json_loads           | 28.9 us                                                    | 27.9 us: 1.04x faster                                               |
| unpickle_pure_python | 218 us                                                     | 212 us: 1.03x faster                                                |
| pickle_dict          | 34.8 us                                                    | 34.0 us: 1.02x faster                                               |
| pickle_pure_python   | 305 us                                                     | 298 us: 1.02x faster                                                |
| pickle_list          | 5.11 us                                                    | 5.00 us: 1.02x faster                                               |
| xml_etree_process    | 61.2 ms                                                    | 59.9 ms: 1.02x faster                                               |
| tomli_loads          | 2.12 sec                                                   | 2.09 sec: 1.01x faster                                              |
| json_dumps           | 10.7 ms                                                    | 10.6 ms: 1.01x faster                                               |
| xml_etree_generate   | 87.4 ms                                                    | 86.9 ms: 1.01x faster                                               |
| pickle               | 11.5 us                                                    | 11.7 us: 1.02x slower                                               |
| unpickle             | 15.1 us                                                    | 17.0 us: 1.12x slower                                               |
| Geometric mean       | (ref)                                                      | 1.01x faster                                                        |

Benchmark hidden because not significant (2): xml_etree_parse, xml_etree_iterparse

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240415-linux-x86_64-gvanrossum-disable_tier2-3.13.0a6+-2055e5f |
|------------------------|:----------------------------------------------------------:|:-------------------------------------------------------------------:|
| python_startup         | 10.8 ms                                                    | 10.6 ms: 1.02x faster                                               |
| python_startup_no_site | 7.11 ms                                                    | 7.12 ms: 1.00x slower                                               |
| Geometric mean         | (ref)                                                      | 1.01x faster                                                        |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240415-linux-x86_64-gvanrossum-disable_tier2-3.13.0a6+-2055e5f |
|-----------------|:----------------------------------------------------------:|:-------------------------------------------------------------------:|
| mako            | 11.2 ms                                                    | 10.8 ms: 1.04x faster                                               |
| django_template | 34.8 ms                                                    | 34.4 ms: 1.01x faster                                               |
| genshi_xml      | 51.6 ms                                                    | 52.4 ms: 1.02x slower                                               |
| Geometric mean  | (ref)                                                      | 1.01x faster                                                        |

Benchmark hidden because not significant (1): genshi_text

All benchmarks:
===============

| Benchmark                  | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240415-linux-x86_64-gvanrossum-disable_tier2-3.13.0a6+-2055e5f |
|----------------------------|:----------------------------------------------------------:|:-------------------------------------------------------------------:|
| typing_runtime_protocols   | 165 us                                                     | 115 us: 1.44x faster                                                |
| richards                   | 50.9 ms                                                    | 46.3 ms: 1.10x faster                                               |
| richards_super             | 57.4 ms                                                    | 52.2 ms: 1.10x faster                                               |
| logging_silent             | 105 ns                                                     | 96.2 ns: 1.09x faster                                               |
| mdp                        | 2.79 sec                                                   | 2.56 sec: 1.09x faster                                              |
| async_tree_none            | 378 ms                                                     | 352 ms: 1.08x faster                                                |
| deepcopy_memo              | 39.7 us                                                    | 37.1 us: 1.07x faster                                               |
| scimark_fft                | 392 ms                                                     | 369 ms: 1.06x faster                                                |
| scimark_sor                | 127 ms                                                     | 120 ms: 1.06x faster                                                |
| deepcopy_reduce            | 3.35 us                                                    | 3.16 us: 1.06x faster                                               |
| scimark_lu                 | 122 ms                                                     | 115 ms: 1.06x faster                                                |
| unpickle_list              | 5.34 us                                                    | 5.07 us: 1.05x faster                                               |
| spectral_norm              | 116 ms                                                     | 111 ms: 1.05x faster                                                |
| deepcopy                   | 367 us                                                     | 351 us: 1.05x faster                                                |
| pyflate                    | 484 ms                                                     | 463 ms: 1.05x faster                                                |
| chameleon                  | 7.22 ms                                                    | 6.91 ms: 1.04x faster                                               |
| mako                       | 11.2 ms                                                    | 10.8 ms: 1.04x faster                                               |
| sqlglot_parse              | 1.32 ms                                                    | 1.27 ms: 1.04x faster                                               |
| create_gc_cycles           | 1.82 ms                                                    | 1.75 ms: 1.04x faster                                               |
| deltablue                  | 3.25 ms                                                    | 3.14 ms: 1.04x faster                                               |
| json_loads                 | 28.9 us                                                    | 27.9 us: 1.04x faster                                               |
| go                         | 145 ms                                                     | 140 ms: 1.04x faster                                                |
| crypto_pyaes               | 77.5 ms                                                    | 74.8 ms: 1.04x faster                                               |
| logging_format             | 6.47 us                                                    | 6.26 us: 1.03x faster                                               |
| chaos                      | 61.3 ms                                                    | 59.5 ms: 1.03x faster                                               |
| nbody                      | 88.3 ms                                                    | 85.7 ms: 1.03x faster                                               |
| unpickle_pure_python       | 218 us                                                     | 212 us: 1.03x faster                                                |
| sqlglot_transpile          | 1.63 ms                                                    | 1.59 ms: 1.03x faster                                               |
| fannkuch                   | 402 ms                                                     | 391 ms: 1.03x faster                                                |
| raytrace                   | 267 ms                                                     | 259 ms: 1.03x faster                                                |
| scimark_monte_carlo        | 69.2 ms                                                    | 67.3 ms: 1.03x faster                                               |
| json                       | 5.31 ms                                                    | 5.16 ms: 1.03x faster                                               |
| comprehensions             | 16.6 us                                                    | 16.2 us: 1.03x faster                                               |
| hexiom                     | 6.30 ms                                                    | 6.13 ms: 1.03x faster                                               |
| pickle_dict                | 34.8 us                                                    | 34.0 us: 1.02x faster                                               |
| pickle_pure_python         | 305 us                                                     | 298 us: 1.02x faster                                                |
| regex_compile              | 137 ms                                                     | 134 ms: 1.02x faster                                                |
| nqueens                    | 81.4 ms                                                    | 79.6 ms: 1.02x faster                                               |
| pickle_list                | 5.11 us                                                    | 5.00 us: 1.02x faster                                               |
| 2to3                       | 274 ms                                                     | 268 ms: 1.02x faster                                                |
| xml_etree_process          | 61.2 ms                                                    | 59.9 ms: 1.02x faster                                               |
| dulwich_log                | 67.2 ms                                                    | 65.9 ms: 1.02x faster                                               |
| scimark_sparse_mat_mult    | 5.27 ms                                                    | 5.17 ms: 1.02x faster                                               |
| sqlite_synth               | 2.99 us                                                    | 2.94 us: 1.02x faster                                               |
| logging_simple             | 5.74 us                                                    | 5.64 us: 1.02x faster                                               |
| pprint_pformat             | 1.56 sec                                                   | 1.53 sec: 1.02x faster                                              |
| python_startup             | 10.8 ms                                                    | 10.6 ms: 1.02x faster                                               |
| float                      | 78.9 ms                                                    | 77.7 ms: 1.02x faster                                               |
| tomli_loads                | 2.12 sec                                                   | 2.09 sec: 1.01x faster                                              |
| sqlglot_optimize           | 55.5 ms                                                    | 54.7 ms: 1.01x faster                                               |
| sympy_integrate            | 20.5 ms                                                    | 20.2 ms: 1.01x faster                                               |
| pprint_safe_repr           | 758 ms                                                     | 749 ms: 1.01x faster                                                |
| docutils                   | 2.83 sec                                                   | 2.79 sec: 1.01x faster                                              |
| sympy_str                  | 282 ms                                                     | 279 ms: 1.01x faster                                                |
| django_template            | 34.8 ms                                                    | 34.4 ms: 1.01x faster                                               |
| meteor_contest             | 110 ms                                                     | 109 ms: 1.01x faster                                                |
| sympy_sum                  | 156 ms                                                     | 154 ms: 1.01x faster                                                |
| sqlglot_normalize          | 110 ms                                                     | 109 ms: 1.01x faster                                                |
| aiohttp                    | 1.18 ms                                                    | 1.17 ms: 1.01x faster                                               |
| generators                 | 29.6 ms                                                    | 29.4 ms: 1.01x faster                                               |
| json_dumps                 | 10.7 ms                                                    | 10.6 ms: 1.01x faster                                               |
| asyncio_tcp                | 508 ms                                                     | 505 ms: 1.01x faster                                                |
| xml_etree_generate         | 87.4 ms                                                    | 86.9 ms: 1.01x faster                                               |
| thrift                     | 823 us                                                     | 818 us: 1.01x faster                                                |
| asyncio_websockets         | 567 ms                                                     | 564 ms: 1.01x faster                                                |
| tornado_http               | 94.6 ms                                                    | 94.3 ms: 1.00x faster                                               |
| asyncio_tcp_ssl            | 1.84 sec                                                   | 1.84 sec: 1.00x faster                                              |
| python_startup_no_site     | 7.11 ms                                                    | 7.12 ms: 1.00x slower                                               |
| async_generators           | 442 ms                                                     | 444 ms: 1.00x slower                                                |
| gc_traversal               | 3.98 ms                                                    | 4.01 ms: 1.01x slower                                               |
| genshi_xml                 | 51.6 ms                                                    | 52.4 ms: 1.02x slower                                               |
| pickle                     | 11.5 us                                                    | 11.7 us: 1.02x slower                                               |
| regex_dna                  | 221 ms                                                     | 226 ms: 1.02x slower                                                |
| async_tree_cpu_io_mixed_tg | 587 ms                                                     | 603 ms: 1.03x slower                                                |
| pathlib                    | 17.3 ms                                                    | 17.8 ms: 1.03x slower                                               |
| regex_v8                   | 25.1 ms                                                    | 25.9 ms: 1.03x slower                                               |
| telco                      | 8.41 ms                                                    | 8.69 ms: 1.03x slower                                               |
| coverage                   | 93.1 ms                                                    | 96.4 ms: 1.03x slower                                               |
| pycparser                  | 1.16 sec                                                   | 1.20 sec: 1.04x slower                                              |
| pidigits                   | 191 ms                                                     | 198 ms: 1.04x slower                                                |
| regex_effbot               | 3.67 ms                                                    | 3.82 ms: 1.04x slower                                               |
| unpickle                   | 15.1 us                                                    | 17.0 us: 1.12x slower                                               |
| Geometric mean             | (ref)                                                      | 1.02x faster                                                        |

Benchmark hidden because not significant (19): async_tree_io_tg, async_tree_io, async_tree_none_tg, async_tree_memoization_tg, dask, djangocms, sympy_expand, gunicorn, xml_etree_parse, mypy2, async_tree_cpu_io_mixed, coroutines, bench_thread_pool, genshi_text, async_tree_memoization, html5lib, xml_etree_iterparse, bench_mp_pool, pylint
Ignored benchmarks (2) of results/bm-20240605-3.13.0b2-3a83b17/bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17.json: bpe_tokeniser, flaskblogging

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 0.98x