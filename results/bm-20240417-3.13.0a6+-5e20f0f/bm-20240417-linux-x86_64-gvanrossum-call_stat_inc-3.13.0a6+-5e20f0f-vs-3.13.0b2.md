# Results vs. 3.13.0b2

- fork: gvanrossum
- ref: call_stat_inc
- machine: linux-x86_64
- commit hash: 5e20f0f
- commit date: 2024-04-17
- overall geometric mean: 1.01x faster
- HPT reliability: 99.99%
- HPT 99th percentile: 1.00x faster
- Memory change: 0.98x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240417-linux-x86_64-gvanrossum-call_stat_inc-3.13.0a6+-5e20f0f |
|----------------|:----------------------------------------------------------:|:-------------------------------------------------------------------:|
| 2to3           | 274 ms                                                     | 269 ms: 1.02x faster                                                |
| chameleon      | 7.22 ms                                                    | 7.10 ms: 1.02x faster                                               |
| html5lib       | 67.2 ms                                                    | 65.8 ms: 1.02x faster                                               |
| tornado_http   | 94.6 ms                                                    | 93.9 ms: 1.01x faster                                               |
| Geometric mean | (ref)                                                      | 1.01x faster                                                        |

Benchmark hidden because not significant (1): docutils

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240417-linux-x86_64-gvanrossum-call_stat_inc-3.13.0a6+-5e20f0f |
|----------------------------|:----------------------------------------------------------:|:-------------------------------------------------------------------:|
| async_tree_none            | 378 ms                                                     | 353 ms: 1.07x faster                                                |
| async_tree_cpu_io_mixed_tg | 587 ms                                                     | 605 ms: 1.03x slower                                                |
| Geometric mean             | (ref)                                                      | 1.01x faster                                                        |

Benchmark hidden because not significant (6): async_tree_io_tg, async_tree_memoization, async_tree_memoization_tg, async_tree_none_tg, async_tree_cpu_io_mixed, async_tree_io

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240417-linux-x86_64-gvanrossum-call_stat_inc-3.13.0a6+-5e20f0f |
|----------------|:----------------------------------------------------------:|:-------------------------------------------------------------------:|
| nbody          | 88.3 ms                                                    | 87.2 ms: 1.01x faster                                               |
| float          | 78.9 ms                                                    | 78.3 ms: 1.01x faster                                               |
| pidigits       | 191 ms                                                     | 190 ms: 1.01x faster                                                |
| Geometric mean | (ref)                                                      | 1.01x faster                                                        |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240417-linux-x86_64-gvanrossum-call_stat_inc-3.13.0a6+-5e20f0f |
|----------------|:----------------------------------------------------------:|:-------------------------------------------------------------------:|
| regex_compile  | 137 ms                                                     | 134 ms: 1.02x faster                                                |
| regex_dna      | 221 ms                                                     | 225 ms: 1.02x slower                                                |
| regex_effbot   | 3.67 ms                                                    | 3.73 ms: 1.02x slower                                               |
| Geometric mean | (ref)                                                      | 1.00x slower                                                        |

Benchmark hidden because not significant (1): regex_v8

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240417-linux-x86_64-gvanrossum-call_stat_inc-3.13.0a6+-5e20f0f |
|----------------------|:----------------------------------------------------------:|:-------------------------------------------------------------------:|
| unpickle_list        | 5.34 us                                                    | 5.03 us: 1.06x faster                                               |
| json_loads           | 28.9 us                                                    | 27.7 us: 1.04x faster                                               |
| unpickle_pure_python | 218 us                                                     | 214 us: 1.02x faster                                                |
| json_dumps           | 10.7 ms                                                    | 10.5 ms: 1.02x faster                                               |
| pickle_dict          | 34.8 us                                                    | 34.3 us: 1.01x faster                                               |
| pickle_pure_python   | 305 us                                                     | 302 us: 1.01x faster                                                |
| xml_etree_process    | 61.2 ms                                                    | 60.9 ms: 1.00x faster                                               |
| xml_etree_generate   | 87.4 ms                                                    | 87.8 ms: 1.00x slower                                               |
| pickle_list          | 5.11 us                                                    | 5.13 us: 1.01x slower                                               |
| tomli_loads          | 2.12 sec                                                   | 2.17 sec: 1.02x slower                                              |
| pickle               | 11.5 us                                                    | 11.9 us: 1.04x slower                                               |
| unpickle             | 15.1 us                                                    | 16.6 us: 1.10x slower                                               |
| Geometric mean       | (ref)                                                      | 1.00x faster                                                        |

Benchmark hidden because not significant (2): xml_etree_parse, xml_etree_iterparse

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240417-linux-x86_64-gvanrossum-call_stat_inc-3.13.0a6+-5e20f0f |
|------------------------|:----------------------------------------------------------:|:-------------------------------------------------------------------:|
| python_startup         | 10.8 ms                                                    | 10.5 ms: 1.02x faster                                               |
| python_startup_no_site | 7.11 ms                                                    | 7.08 ms: 1.00x faster                                               |
| Geometric mean         | (ref)                                                      | 1.01x faster                                                        |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240417-linux-x86_64-gvanrossum-call_stat_inc-3.13.0a6+-5e20f0f |
|-----------------|:----------------------------------------------------------:|:-------------------------------------------------------------------:|
| mako            | 11.2 ms                                                    | 10.7 ms: 1.05x faster                                               |
| genshi_text     | 23.7 ms                                                    | 23.3 ms: 1.02x faster                                               |
| genshi_xml      | 51.6 ms                                                    | 51.4 ms: 1.00x faster                                               |
| django_template | 34.8 ms                                                    | 35.5 ms: 1.02x slower                                               |
| Geometric mean  | (ref)                                                      | 1.01x faster                                                        |

All benchmarks:
===============

| Benchmark                  | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240417-linux-x86_64-gvanrossum-call_stat_inc-3.13.0a6+-5e20f0f |
|----------------------------|:----------------------------------------------------------:|:-------------------------------------------------------------------:|
| typing_runtime_protocols   | 165 us                                                     | 113 us: 1.45x faster                                                |
| richards_super             | 57.4 ms                                                    | 52.7 ms: 1.09x faster                                               |
| gc_traversal               | 3.98 ms                                                    | 3.68 ms: 1.08x faster                                               |
| richards                   | 50.9 ms                                                    | 47.3 ms: 1.08x faster                                               |
| deepcopy_memo              | 39.7 us                                                    | 37.0 us: 1.07x faster                                               |
| async_tree_none            | 378 ms                                                     | 353 ms: 1.07x faster                                                |
| unpickle_list              | 5.34 us                                                    | 5.03 us: 1.06x faster                                               |
| crypto_pyaes               | 77.5 ms                                                    | 73.5 ms: 1.05x faster                                               |
| scimark_lu                 | 122 ms                                                     | 115 ms: 1.05x faster                                                |
| mako                       | 11.2 ms                                                    | 10.7 ms: 1.05x faster                                               |
| json_loads                 | 28.9 us                                                    | 27.7 us: 1.04x faster                                               |
| create_gc_cycles           | 1.82 ms                                                    | 1.74 ms: 1.04x faster                                               |
| pyflate                    | 484 ms                                                     | 465 ms: 1.04x faster                                                |
| deepcopy_reduce            | 3.35 us                                                    | 3.22 us: 1.04x faster                                               |
| logging_silent             | 105 ns                                                     | 101 ns: 1.04x faster                                                |
| mdp                        | 2.79 sec                                                   | 2.68 sec: 1.04x faster                                              |
| scimark_fft                | 392 ms                                                     | 378 ms: 1.04x faster                                                |
| scimark_sor                | 127 ms                                                     | 123 ms: 1.04x faster                                                |
| sqlglot_transpile          | 1.63 ms                                                    | 1.58 ms: 1.04x faster                                               |
| sqlglot_parse              | 1.32 ms                                                    | 1.28 ms: 1.03x faster                                               |
| deepcopy                   | 367 us                                                     | 356 us: 1.03x faster                                                |
| hexiom                     | 6.30 ms                                                    | 6.14 ms: 1.03x faster                                               |
| python_startup             | 10.8 ms                                                    | 10.5 ms: 1.02x faster                                               |
| json                       | 5.31 ms                                                    | 5.18 ms: 1.02x faster                                               |
| go                         | 145 ms                                                     | 141 ms: 1.02x faster                                                |
| coroutines                 | 23.2 ms                                                    | 22.7 ms: 1.02x faster                                               |
| html5lib                   | 67.2 ms                                                    | 65.8 ms: 1.02x faster                                               |
| fannkuch                   | 402 ms                                                     | 394 ms: 1.02x faster                                                |
| regex_compile              | 137 ms                                                     | 134 ms: 1.02x faster                                                |
| 2to3                       | 274 ms                                                     | 269 ms: 1.02x faster                                                |
| scimark_sparse_mat_mult    | 5.27 ms                                                    | 5.17 ms: 1.02x faster                                               |
| unpickle_pure_python       | 218 us                                                     | 214 us: 1.02x faster                                                |
| dulwich_log                | 67.2 ms                                                    | 66.0 ms: 1.02x faster                                               |
| json_dumps                 | 10.7 ms                                                    | 10.5 ms: 1.02x faster                                               |
| genshi_text                | 23.7 ms                                                    | 23.3 ms: 1.02x faster                                               |
| chameleon                  | 7.22 ms                                                    | 7.10 ms: 1.02x faster                                               |
| pickle_dict                | 34.8 us                                                    | 34.3 us: 1.01x faster                                               |
| chaos                      | 61.3 ms                                                    | 60.5 ms: 1.01x faster                                               |
| scimark_monte_carlo        | 69.2 ms                                                    | 68.2 ms: 1.01x faster                                               |
| deltablue                  | 3.25 ms                                                    | 3.21 ms: 1.01x faster                                               |
| nbody                      | 88.3 ms                                                    | 87.2 ms: 1.01x faster                                               |
| raytrace                   | 267 ms                                                     | 264 ms: 1.01x faster                                                |
| aiohttp                    | 1.18 ms                                                    | 1.17 ms: 1.01x faster                                               |
| pprint_pformat             | 1.56 sec                                                   | 1.54 sec: 1.01x faster                                              |
| pickle_pure_python         | 305 us                                                     | 302 us: 1.01x faster                                                |
| thrift                     | 823 us                                                     | 816 us: 1.01x faster                                                |
| spectral_norm              | 116 ms                                                     | 115 ms: 1.01x faster                                                |
| tornado_http               | 94.6 ms                                                    | 93.9 ms: 1.01x faster                                               |
| float                      | 78.9 ms                                                    | 78.3 ms: 1.01x faster                                               |
| meteor_contest             | 110 ms                                                     | 109 ms: 1.01x faster                                                |
| gunicorn                   | 1.28 ms                                                    | 1.27 ms: 1.01x faster                                               |
| pidigits                   | 191 ms                                                     | 190 ms: 1.01x faster                                                |
| xml_etree_process          | 61.2 ms                                                    | 60.9 ms: 1.00x faster                                               |
| genshi_xml                 | 51.6 ms                                                    | 51.4 ms: 1.00x faster                                               |
| asyncio_tcp                | 508 ms                                                     | 506 ms: 1.00x faster                                                |
| python_startup_no_site     | 7.11 ms                                                    | 7.08 ms: 1.00x faster                                               |
| sqlglot_optimize           | 55.5 ms                                                    | 55.3 ms: 1.00x faster                                               |
| sympy_integrate            | 20.5 ms                                                    | 20.4 ms: 1.00x faster                                               |
| xml_etree_generate         | 87.4 ms                                                    | 87.8 ms: 1.00x slower                                               |
| logging_format             | 6.47 us                                                    | 6.50 us: 1.00x slower                                               |
| pickle_list                | 5.11 us                                                    | 5.13 us: 1.01x slower                                               |
| sqlglot_normalize          | 110 ms                                                     | 111 ms: 1.01x slower                                                |
| nqueens                    | 81.4 ms                                                    | 81.9 ms: 1.01x slower                                               |
| sympy_sum                  | 156 ms                                                     | 157 ms: 1.01x slower                                                |
| async_generators           | 442 ms                                                     | 447 ms: 1.01x slower                                                |
| comprehensions             | 16.6 us                                                    | 16.8 us: 1.01x slower                                               |
| regex_dna                  | 221 ms                                                     | 225 ms: 1.02x slower                                                |
| regex_effbot               | 3.67 ms                                                    | 3.73 ms: 1.02x slower                                               |
| logging_simple             | 5.74 us                                                    | 5.85 us: 1.02x slower                                               |
| django_template            | 34.8 ms                                                    | 35.5 ms: 1.02x slower                                               |
| tomli_loads                | 2.12 sec                                                   | 2.17 sec: 1.02x slower                                              |
| pathlib                    | 17.3 ms                                                    | 17.8 ms: 1.03x slower                                               |
| async_tree_cpu_io_mixed_tg | 587 ms                                                     | 605 ms: 1.03x slower                                                |
| telco                      | 8.41 ms                                                    | 8.71 ms: 1.04x slower                                               |
| pickle                     | 11.5 us                                                    | 11.9 us: 1.04x slower                                               |
| coverage                   | 93.1 ms                                                    | 98.0 ms: 1.05x slower                                               |
| unpickle                   | 15.1 us                                                    | 16.6 us: 1.10x slower                                               |
| Geometric mean             | (ref)                                                      | 1.01x faster                                                        |

Benchmark hidden because not significant (24): async_tree_io_tg, mypy2, async_tree_memoization, dask, xml_etree_parse, async_tree_memoization_tg, djangocms, docutils, regex_v8, pprint_safe_repr, sqlite_synth, pycparser, sympy_str, async_tree_none_tg, xml_etree_iterparse, asyncio_tcp_ssl, async_tree_cpu_io_mixed, bench_mp_pool, bench_thread_pool, generators, async_tree_io, asyncio_websockets, sympy_expand, pylint
Ignored benchmarks (2) of results/bm-20240605-3.13.0b2-3a83b17/bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17.json: bpe_tokeniser, flaskblogging

# HPT report

- Reliability score: 99.99% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 0.98x