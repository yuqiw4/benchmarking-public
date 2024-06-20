# Results vs. 3.13.0b2

- fork: faster-cpython
- ref: call_cmethod
- machine: linux-x86_64
- commit hash: 5c20c52
- commit date: 2024-04-10
- overall geometric mean: 1.01x faster
- HPT reliability: 99.95%
- HPT 99th percentile: 1.00x faster
- Memory change: 0.98x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240410-linux-x86_64-faster%2dcpython-call_cmethod-3.13.0a5+-5c20c52 |
|----------------|:----------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 274 ms                                                     | 271 ms: 1.01x faster                                                     |
| chameleon      | 7.22 ms                                                    | 7.03 ms: 1.03x faster                                                    |
| docutils       | 2.83 sec                                                   | 2.84 sec: 1.01x slower                                                   |
| html5lib       | 67.2 ms                                                    | 67.8 ms: 1.01x slower                                                    |
| Geometric mean | (ref)                                                      | 1.00x faster                                                             |

Benchmark hidden because not significant (1): tornado_http

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240410-linux-x86_64-faster%2dcpython-call_cmethod-3.13.0a5+-5c20c52 |
|----------------------------|:----------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_none            | 378 ms                                                     | 346 ms: 1.09x faster                                                     |
| async_tree_cpu_io_mixed_tg | 587 ms                                                     | 601 ms: 1.02x slower                                                     |
| Geometric mean             | (ref)                                                      | 1.02x faster                                                             |

Benchmark hidden because not significant (6): async_tree_io, async_tree_io_tg, async_tree_memoization, async_tree_cpu_io_mixed, async_tree_none_tg, async_tree_memoization_tg

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240410-linux-x86_64-faster%2dcpython-call_cmethod-3.13.0a5+-5c20c52 |
|----------------|:----------------------------------------------------------:|:------------------------------------------------------------------------:|
| pidigits       | 191 ms                                                     | 190 ms: 1.01x faster                                                     |
| Geometric mean | (ref)                                                      | 1.00x faster                                                             |

Benchmark hidden because not significant (2): float, nbody

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240410-linux-x86_64-faster%2dcpython-call_cmethod-3.13.0a5+-5c20c52 |
|----------------|:----------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_v8       | 25.1 ms                                                    | 24.2 ms: 1.04x faster                                                    |
| regex_dna      | 221 ms                                                     | 218 ms: 1.01x faster                                                     |
| regex_compile  | 137 ms                                                     | 135 ms: 1.01x faster                                                     |
| regex_effbot   | 3.67 ms                                                    | 3.70 ms: 1.01x slower                                                    |
| Geometric mean | (ref)                                                      | 1.01x faster                                                             |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240410-linux-x86_64-faster%2dcpython-call_cmethod-3.13.0a5+-5c20c52 |
|----------------------|:----------------------------------------------------------:|:------------------------------------------------------------------------:|
| json_dumps           | 10.7 ms                                                    | 10.5 ms: 1.02x faster                                                    |
| unpickle_list        | 5.34 us                                                    | 5.25 us: 1.02x faster                                                    |
| json_loads           | 28.9 us                                                    | 28.4 us: 1.02x faster                                                    |
| pickle_pure_python   | 305 us                                                     | 302 us: 1.01x faster                                                     |
| pickle_list          | 5.11 us                                                    | 5.07 us: 1.01x faster                                                    |
| pickle_dict          | 34.8 us                                                    | 34.9 us: 1.00x slower                                                    |
| xml_etree_generate   | 87.4 ms                                                    | 88.3 ms: 1.01x slower                                                    |
| pickle               | 11.5 us                                                    | 11.6 us: 1.01x slower                                                    |
| tomli_loads          | 2.12 sec                                                   | 2.15 sec: 1.01x slower                                                   |
| unpickle_pure_python | 218 us                                                     | 222 us: 1.02x slower                                                     |
| Geometric mean       | (ref)                                                      | 1.00x faster                                                             |

Benchmark hidden because not significant (4): xml_etree_parse, xml_etree_iterparse, unpickle, xml_etree_process

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240410-linux-x86_64-faster%2dcpython-call_cmethod-3.13.0a5+-5c20c52 |
|------------------------|:----------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup         | 10.8 ms                                                    | 10.5 ms: 1.02x faster                                                    |
| python_startup_no_site | 7.11 ms                                                    | 8.95 ms: 1.26x slower                                                    |
| Geometric mean         | (ref)                                                      | 1.11x slower                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark      | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240410-linux-x86_64-faster%2dcpython-call_cmethod-3.13.0a5+-5c20c52 |
|----------------|:----------------------------------------------------------:|:------------------------------------------------------------------------:|
| mako           | 11.2 ms                                                    | 10.8 ms: 1.04x faster                                                    |
| genshi_text    | 23.7 ms                                                    | 23.9 ms: 1.01x slower                                                    |
| genshi_xml     | 51.6 ms                                                    | 52.9 ms: 1.03x slower                                                    |
| Geometric mean | (ref)                                                      | 1.00x faster                                                             |

All benchmarks:
===============

| Benchmark                  | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240410-linux-x86_64-faster%2dcpython-call_cmethod-3.13.0a5+-5c20c52 |
|----------------------------|:----------------------------------------------------------:|:------------------------------------------------------------------------:|
| typing_runtime_protocols   | 165 us                                                     | 117 us: 1.41x faster                                                     |
| pylint                     | 317 ms                                                     | 279 ms: 1.14x faster                                                     |
| async_tree_none            | 378 ms                                                     | 346 ms: 1.09x faster                                                     |
| scimark_fft                | 392 ms                                                     | 360 ms: 1.09x faster                                                     |
| richards_super             | 57.4 ms                                                    | 52.9 ms: 1.08x faster                                                    |
| richards                   | 50.9 ms                                                    | 47.0 ms: 1.08x faster                                                    |
| scimark_lu                 | 122 ms                                                     | 113 ms: 1.08x faster                                                     |
| deepcopy_reduce            | 3.35 us                                                    | 3.19 us: 1.05x faster                                                    |
| gc_traversal               | 3.98 ms                                                    | 3.79 ms: 1.05x faster                                                    |
| mako                       | 11.2 ms                                                    | 10.8 ms: 1.04x faster                                                    |
| create_gc_cycles           | 1.82 ms                                                    | 1.75 ms: 1.04x faster                                                    |
| logging_silent             | 105 ns                                                     | 101 ns: 1.04x faster                                                     |
| regex_v8                   | 25.1 ms                                                    | 24.2 ms: 1.04x faster                                                    |
| go                         | 145 ms                                                     | 140 ms: 1.04x faster                                                     |
| scimark_sor                | 127 ms                                                     | 123 ms: 1.03x faster                                                     |
| fannkuch                   | 402 ms                                                     | 389 ms: 1.03x faster                                                     |
| coroutines                 | 23.2 ms                                                    | 22.5 ms: 1.03x faster                                                    |
| deepcopy_memo              | 39.7 us                                                    | 38.5 us: 1.03x faster                                                    |
| sqlglot_transpile          | 1.63 ms                                                    | 1.59 ms: 1.03x faster                                                    |
| chameleon                  | 7.22 ms                                                    | 7.03 ms: 1.03x faster                                                    |
| sqlglot_parse              | 1.32 ms                                                    | 1.29 ms: 1.03x faster                                                    |
| scimark_monte_carlo        | 69.2 ms                                                    | 67.4 ms: 1.03x faster                                                    |
| deepcopy                   | 367 us                                                     | 359 us: 1.02x faster                                                     |
| python_startup             | 10.8 ms                                                    | 10.5 ms: 1.02x faster                                                    |
| json_dumps                 | 10.7 ms                                                    | 10.5 ms: 1.02x faster                                                    |
| asyncio_tcp                | 508 ms                                                     | 498 ms: 1.02x faster                                                     |
| deltablue                  | 3.25 ms                                                    | 3.19 ms: 1.02x faster                                                    |
| sqlite_synth               | 2.99 us                                                    | 2.93 us: 1.02x faster                                                    |
| raytrace                   | 267 ms                                                     | 262 ms: 1.02x faster                                                     |
| unpickle_list              | 5.34 us                                                    | 5.25 us: 1.02x faster                                                    |
| hexiom                     | 6.30 ms                                                    | 6.18 ms: 1.02x faster                                                    |
| json_loads                 | 28.9 us                                                    | 28.4 us: 1.02x faster                                                    |
| pyflate                    | 484 ms                                                     | 476 ms: 1.02x faster                                                     |
| regex_dna                  | 221 ms                                                     | 218 ms: 1.01x faster                                                     |
| pprint_pformat             | 1.56 sec                                                   | 1.53 sec: 1.01x faster                                                   |
| logging_format             | 6.47 us                                                    | 6.39 us: 1.01x faster                                                    |
| 2to3                       | 274 ms                                                     | 271 ms: 1.01x faster                                                     |
| pprint_safe_repr           | 758 ms                                                     | 749 ms: 1.01x faster                                                     |
| pickle_pure_python         | 305 us                                                     | 302 us: 1.01x faster                                                     |
| chaos                      | 61.3 ms                                                    | 60.6 ms: 1.01x faster                                                    |
| regex_compile              | 137 ms                                                     | 135 ms: 1.01x faster                                                     |
| crypto_pyaes               | 77.5 ms                                                    | 76.6 ms: 1.01x faster                                                    |
| sympy_str                  | 282 ms                                                     | 279 ms: 1.01x faster                                                     |
| thrift                     | 823 us                                                     | 815 us: 1.01x faster                                                     |
| aiohttp                    | 1.18 ms                                                    | 1.17 ms: 1.01x faster                                                    |
| pidigits                   | 191 ms                                                     | 190 ms: 1.01x faster                                                     |
| pickle_list                | 5.11 us                                                    | 5.07 us: 1.01x faster                                                    |
| sqlglot_optimize           | 55.5 ms                                                    | 55.2 ms: 1.01x faster                                                    |
| mdp                        | 2.79 sec                                                   | 2.77 sec: 1.01x faster                                                   |
| nqueens                    | 81.4 ms                                                    | 80.9 ms: 1.01x faster                                                    |
| sympy_integrate            | 20.5 ms                                                    | 20.4 ms: 1.00x faster                                                    |
| dulwich_log                | 67.2 ms                                                    | 66.9 ms: 1.00x faster                                                    |
| asyncio_tcp_ssl            | 1.84 sec                                                   | 1.84 sec: 1.00x faster                                                   |
| pickle_dict                | 34.8 us                                                    | 34.9 us: 1.00x slower                                                    |
| docutils                   | 2.83 sec                                                   | 2.84 sec: 1.01x slower                                                   |
| sympy_sum                  | 156 ms                                                     | 157 ms: 1.01x slower                                                     |
| meteor_contest             | 110 ms                                                     | 111 ms: 1.01x slower                                                     |
| async_generators           | 442 ms                                                     | 445 ms: 1.01x slower                                                     |
| regex_effbot               | 3.67 ms                                                    | 3.70 ms: 1.01x slower                                                    |
| html5lib                   | 67.2 ms                                                    | 67.8 ms: 1.01x slower                                                    |
| genshi_text                | 23.7 ms                                                    | 23.9 ms: 1.01x slower                                                    |
| xml_etree_generate         | 87.4 ms                                                    | 88.3 ms: 1.01x slower                                                    |
| json                       | 5.31 ms                                                    | 5.36 ms: 1.01x slower                                                    |
| pickle                     | 11.5 us                                                    | 11.6 us: 1.01x slower                                                    |
| tomli_loads                | 2.12 sec                                                   | 2.15 sec: 1.01x slower                                                   |
| logging_simple             | 5.74 us                                                    | 5.85 us: 1.02x slower                                                    |
| unpickle_pure_python       | 218 us                                                     | 222 us: 1.02x slower                                                     |
| async_tree_cpu_io_mixed_tg | 587 ms                                                     | 601 ms: 1.02x slower                                                     |
| genshi_xml                 | 51.6 ms                                                    | 52.9 ms: 1.03x slower                                                    |
| telco                      | 8.41 ms                                                    | 8.70 ms: 1.03x slower                                                    |
| coverage                   | 93.1 ms                                                    | 96.8 ms: 1.04x slower                                                    |
| pathlib                    | 17.3 ms                                                    | 19.0 ms: 1.10x slower                                                    |
| python_startup_no_site     | 7.11 ms                                                    | 8.95 ms: 1.26x slower                                                    |
| Geometric mean             | (ref)                                                      | 1.01x faster                                                             |

Benchmark hidden because not significant (26): async_tree_io, async_tree_io_tg, xml_etree_parse, async_tree_memoization, pycparser, async_tree_cpu_io_mixed, xml_etree_iterparse, async_tree_none_tg, mypy2, gunicorn, unpickle, async_tree_memoization_tg, float, spectral_norm, xml_etree_process, dask, bench_thread_pool, sympy_expand, asyncio_websockets, bench_mp_pool, tornado_http, comprehensions, nbody, generators, sqlglot_normalize, scimark_sparse_mat_mult
Ignored benchmarks (4) of results/bm-20240605-3.13.0b2-3a83b17/bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17.json: bpe_tokeniser, django_template, djangocms, flaskblogging

# HPT report

- Reliability score: 99.95% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 0.98x