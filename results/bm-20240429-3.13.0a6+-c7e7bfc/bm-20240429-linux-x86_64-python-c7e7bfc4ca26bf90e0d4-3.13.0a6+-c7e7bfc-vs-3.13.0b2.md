# Results vs. 3.13.0b2

- fork: python
- ref: c7e7bfc4ca26bf90e0d4
- machine: linux-x86_64
- commit hash: c7e7bfc
- commit date: 2024-04-29
- overall geometric mean: 1.02x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.00x faster
- Memory change: 0.98x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240429-linux-x86_64-python-c7e7bfc4ca26bf90e0d4-3.13.0a6+-c7e7bfc |
|----------------|:----------------------------------------------------------:|:----------------------------------------------------------------------:|
| 2to3           | 274 ms                                                     | 267 ms: 1.02x faster                                                   |
| chameleon      | 7.22 ms                                                    | 6.95 ms: 1.04x faster                                                  |
| docutils       | 2.83 sec                                                   | 2.81 sec: 1.01x faster                                                 |
| html5lib       | 67.2 ms                                                    | 66.2 ms: 1.02x faster                                                  |
| tornado_http   | 94.6 ms                                                    | 93.6 ms: 1.01x faster                                                  |
| Geometric mean | (ref)                                                      | 1.02x faster                                                           |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240429-linux-x86_64-python-c7e7bfc4ca26bf90e0d4-3.13.0a6+-c7e7bfc |
|----------------------------|:----------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_none            | 378 ms                                                     | 350 ms: 1.08x faster                                                   |
| async_tree_cpu_io_mixed_tg | 587 ms                                                     | 604 ms: 1.03x slower                                                   |
| Geometric mean             | (ref)                                                      | 1.01x faster                                                           |

Benchmark hidden because not significant (6): async_tree_memoization_tg, async_tree_none_tg, async_tree_io, async_tree_io_tg, async_tree_cpu_io_mixed, async_tree_memoization

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240429-linux-x86_64-python-c7e7bfc4ca26bf90e0d4-3.13.0a6+-c7e7bfc |
|----------------|:----------------------------------------------------------:|:----------------------------------------------------------------------:|
| float          | 78.9 ms                                                    | 78.0 ms: 1.01x faster                                                  |
| pidigits       | 191 ms                                                     | 212 ms: 1.11x slower                                                   |
| Geometric mean | (ref)                                                      | 1.03x slower                                                           |

Benchmark hidden because not significant (1): nbody

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240429-linux-x86_64-python-c7e7bfc4ca26bf90e0d4-3.13.0a6+-c7e7bfc |
|----------------|:----------------------------------------------------------:|:----------------------------------------------------------------------:|
| regex_compile  | 137 ms                                                     | 134 ms: 1.02x faster                                                   |
| regex_v8       | 25.1 ms                                                    | 24.9 ms: 1.01x faster                                                  |
| regex_effbot   | 3.67 ms                                                    | 3.65 ms: 1.01x faster                                                  |
| regex_dna      | 221 ms                                                     | 225 ms: 1.02x slower                                                   |
| Geometric mean | (ref)                                                      | 1.01x faster                                                           |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240429-linux-x86_64-python-c7e7bfc4ca26bf90e0d4-3.13.0a6+-c7e7bfc |
|----------------------|:----------------------------------------------------------:|:----------------------------------------------------------------------:|
| json_loads           | 28.9 us                                                    | 27.3 us: 1.06x faster                                                  |
| unpickle_list        | 5.34 us                                                    | 5.17 us: 1.03x faster                                                  |
| xml_etree_process    | 61.2 ms                                                    | 59.4 ms: 1.03x faster                                                  |
| unpickle_pure_python | 218 us                                                     | 212 us: 1.03x faster                                                   |
| pickle_list          | 5.11 us                                                    | 5.00 us: 1.02x faster                                                  |
| xml_etree_parse      | 162 ms                                                     | 159 ms: 1.02x faster                                                   |
| pickle_pure_python   | 305 us                                                     | 301 us: 1.01x faster                                                   |
| xml_etree_generate   | 87.4 ms                                                    | 86.3 ms: 1.01x faster                                                  |
| json_dumps           | 10.7 ms                                                    | 10.6 ms: 1.01x faster                                                  |
| unpickle             | 15.1 us                                                    | 15.1 us: 1.00x faster                                                  |
| tomli_loads          | 2.12 sec                                                   | 2.14 sec: 1.01x slower                                                 |
| pickle_dict          | 34.8 us                                                    | 35.4 us: 1.02x slower                                                  |
| pickle               | 11.5 us                                                    | 11.7 us: 1.02x slower                                                  |
| Geometric mean       | (ref)                                                      | 1.01x faster                                                           |

Benchmark hidden because not significant (1): xml_etree_iterparse

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240429-linux-x86_64-python-c7e7bfc4ca26bf90e0d4-3.13.0a6+-c7e7bfc |
|------------------------|:----------------------------------------------------------:|:----------------------------------------------------------------------:|
| python_startup         | 10.8 ms                                                    | 10.5 ms: 1.02x faster                                                  |
| python_startup_no_site | 7.11 ms                                                    | 7.11 ms: 1.00x slower                                                  |
| Geometric mean         | (ref)                                                      | 1.01x faster                                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240429-linux-x86_64-python-c7e7bfc4ca26bf90e0d4-3.13.0a6+-c7e7bfc |
|-----------------|:----------------------------------------------------------:|:----------------------------------------------------------------------:|
| mako            | 11.2 ms                                                    | 10.9 ms: 1.03x faster                                                  |
| genshi_text     | 23.7 ms                                                    | 23.2 ms: 1.02x faster                                                  |
| django_template | 34.8 ms                                                    | 35.0 ms: 1.01x slower                                                  |
| genshi_xml      | 51.6 ms                                                    | 52.0 ms: 1.01x slower                                                  |
| Geometric mean  | (ref)                                                      | 1.01x faster                                                           |

All benchmarks:
===============

| Benchmark                  | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240429-linux-x86_64-python-c7e7bfc4ca26bf90e0d4-3.13.0a6+-c7e7bfc |
|----------------------------|:----------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_none            | 378 ms                                                     | 350 ms: 1.08x faster                                                   |
| richards                   | 50.9 ms                                                    | 47.3 ms: 1.08x faster                                                  |
| gc_traversal               | 3.98 ms                                                    | 3.70 ms: 1.07x faster                                                  |
| scimark_fft                | 392 ms                                                     | 366 ms: 1.07x faster                                                   |
| richards_super             | 57.4 ms                                                    | 53.7 ms: 1.07x faster                                                  |
| scimark_lu                 | 122 ms                                                     | 115 ms: 1.06x faster                                                   |
| json_loads                 | 28.9 us                                                    | 27.3 us: 1.06x faster                                                  |
| mdp                        | 2.79 sec                                                   | 2.64 sec: 1.06x faster                                                 |
| deepcopy_memo              | 39.7 us                                                    | 37.6 us: 1.06x faster                                                  |
| pyflate                    | 484 ms                                                     | 461 ms: 1.05x faster                                                   |
| scimark_sor                | 127 ms                                                     | 122 ms: 1.05x faster                                                   |
| spectral_norm              | 116 ms                                                     | 111 ms: 1.05x faster                                                   |
| deepcopy_reduce            | 3.35 us                                                    | 3.21 us: 1.04x faster                                                  |
| fannkuch                   | 402 ms                                                     | 385 ms: 1.04x faster                                                   |
| create_gc_cycles           | 1.82 ms                                                    | 1.74 ms: 1.04x faster                                                  |
| deepcopy                   | 367 us                                                     | 353 us: 1.04x faster                                                   |
| chameleon                  | 7.22 ms                                                    | 6.95 ms: 1.04x faster                                                  |
| coroutines                 | 23.2 ms                                                    | 22.4 ms: 1.04x faster                                                  |
| crypto_pyaes               | 77.5 ms                                                    | 74.7 ms: 1.04x faster                                                  |
| pprint_safe_repr           | 758 ms                                                     | 732 ms: 1.04x faster                                                   |
| sqlglot_parse              | 1.32 ms                                                    | 1.28 ms: 1.04x faster                                                  |
| logging_silent             | 105 ns                                                     | 101 ns: 1.04x faster                                                   |
| json                       | 5.31 ms                                                    | 5.13 ms: 1.03x faster                                                  |
| unpickle_list              | 5.34 us                                                    | 5.17 us: 1.03x faster                                                  |
| pprint_pformat             | 1.56 sec                                                   | 1.51 sec: 1.03x faster                                                 |
| mako                       | 11.2 ms                                                    | 10.9 ms: 1.03x faster                                                  |
| sqlglot_transpile          | 1.63 ms                                                    | 1.59 ms: 1.03x faster                                                  |
| xml_etree_process          | 61.2 ms                                                    | 59.4 ms: 1.03x faster                                                  |
| unpickle_pure_python       | 218 us                                                     | 212 us: 1.03x faster                                                   |
| hexiom                     | 6.30 ms                                                    | 6.13 ms: 1.03x faster                                                  |
| 2to3                       | 274 ms                                                     | 267 ms: 1.02x faster                                                   |
| regex_compile              | 137 ms                                                     | 134 ms: 1.02x faster                                                   |
| sqlite_synth               | 2.99 us                                                    | 2.92 us: 1.02x faster                                                  |
| coverage                   | 93.1 ms                                                    | 91.0 ms: 1.02x faster                                                  |
| logging_format             | 6.47 us                                                    | 6.33 us: 1.02x faster                                                  |
| pickle_list                | 5.11 us                                                    | 5.00 us: 1.02x faster                                                  |
| go                         | 145 ms                                                     | 142 ms: 1.02x faster                                                   |
| python_startup             | 10.8 ms                                                    | 10.5 ms: 1.02x faster                                                  |
| sympy_str                  | 282 ms                                                     | 277 ms: 1.02x faster                                                   |
| xml_etree_parse            | 162 ms                                                     | 159 ms: 1.02x faster                                                   |
| raytrace                   | 267 ms                                                     | 261 ms: 1.02x faster                                                   |
| aiohttp                    | 1.18 ms                                                    | 1.16 ms: 1.02x faster                                                  |
| genshi_text                | 23.7 ms                                                    | 23.2 ms: 1.02x faster                                                  |
| sympy_expand               | 473 ms                                                     | 464 ms: 1.02x faster                                                   |
| sympy_integrate            | 20.5 ms                                                    | 20.1 ms: 1.02x faster                                                  |
| dulwich_log                | 67.2 ms                                                    | 66.1 ms: 1.02x faster                                                  |
| sqlglot_optimize           | 55.5 ms                                                    | 54.6 ms: 1.02x faster                                                  |
| sympy_sum                  | 156 ms                                                     | 153 ms: 1.02x faster                                                   |
| html5lib                   | 67.2 ms                                                    | 66.2 ms: 1.02x faster                                                  |
| chaos                      | 61.3 ms                                                    | 60.4 ms: 1.02x faster                                                  |
| pickle_pure_python         | 305 us                                                     | 301 us: 1.01x faster                                                   |
| deltablue                  | 3.25 ms                                                    | 3.21 ms: 1.01x faster                                                  |
| gunicorn                   | 1.28 ms                                                    | 1.26 ms: 1.01x faster                                                  |
| xml_etree_generate         | 87.4 ms                                                    | 86.3 ms: 1.01x faster                                                  |
| json_dumps                 | 10.7 ms                                                    | 10.6 ms: 1.01x faster                                                  |
| float                      | 78.9 ms                                                    | 78.0 ms: 1.01x faster                                                  |
| sqlglot_normalize          | 110 ms                                                     | 109 ms: 1.01x faster                                                   |
| bench_mp_pool              | 23.9 ms                                                    | 23.6 ms: 1.01x faster                                                  |
| tornado_http               | 94.6 ms                                                    | 93.6 ms: 1.01x faster                                                  |
| thrift                     | 823 us                                                     | 815 us: 1.01x faster                                                   |
| regex_v8                   | 25.1 ms                                                    | 24.9 ms: 1.01x faster                                                  |
| scimark_sparse_mat_mult    | 5.27 ms                                                    | 5.22 ms: 1.01x faster                                                  |
| scimark_monte_carlo        | 69.2 ms                                                    | 68.6 ms: 1.01x faster                                                  |
| bench_thread_pool          | 834 us                                                     | 827 us: 1.01x faster                                                   |
| docutils                   | 2.83 sec                                                   | 2.81 sec: 1.01x faster                                                 |
| regex_effbot               | 3.67 ms                                                    | 3.65 ms: 1.01x faster                                                  |
| asyncio_websockets         | 567 ms                                                     | 564 ms: 1.00x faster                                                   |
| asyncio_tcp                | 508 ms                                                     | 506 ms: 1.00x faster                                                   |
| unpickle                   | 15.1 us                                                    | 15.1 us: 1.00x faster                                                  |
| python_startup_no_site     | 7.11 ms                                                    | 7.11 ms: 1.00x slower                                                  |
| asyncio_tcp_ssl            | 1.84 sec                                                   | 1.84 sec: 1.00x slower                                                 |
| meteor_contest             | 110 ms                                                     | 110 ms: 1.00x slower                                                   |
| nqueens                    | 81.4 ms                                                    | 81.9 ms: 1.01x slower                                                  |
| django_template            | 34.8 ms                                                    | 35.0 ms: 1.01x slower                                                  |
| genshi_xml                 | 51.6 ms                                                    | 52.0 ms: 1.01x slower                                                  |
| async_generators           | 442 ms                                                     | 446 ms: 1.01x slower                                                   |
| tomli_loads                | 2.12 sec                                                   | 2.14 sec: 1.01x slower                                                 |
| generators                 | 29.6 ms                                                    | 29.9 ms: 1.01x slower                                                  |
| pathlib                    | 17.3 ms                                                    | 17.6 ms: 1.02x slower                                                  |
| regex_dna                  | 221 ms                                                     | 225 ms: 1.02x slower                                                   |
| comprehensions             | 16.6 us                                                    | 16.9 us: 1.02x slower                                                  |
| pickle_dict                | 34.8 us                                                    | 35.4 us: 1.02x slower                                                  |
| pickle                     | 11.5 us                                                    | 11.7 us: 1.02x slower                                                  |
| telco                      | 8.41 ms                                                    | 8.62 ms: 1.02x slower                                                  |
| async_tree_cpu_io_mixed_tg | 587 ms                                                     | 604 ms: 1.03x slower                                                   |
| pidigits                   | 191 ms                                                     | 212 ms: 1.11x slower                                                   |
| Geometric mean             | (ref)                                                      | 1.02x faster                                                           |

Benchmark hidden because not significant (15): async_tree_memoization_tg, async_tree_none_tg, mypy2, async_tree_io, dask, pycparser, xml_etree_iterparse, typing_runtime_protocols, logging_simple, nbody, async_tree_io_tg, pylint, async_tree_cpu_io_mixed, async_tree_memoization, djangocms
Ignored benchmarks (2) of results/bm-20240605-3.13.0b2-3a83b17/bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17.json: bpe_tokeniser, flaskblogging

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.01x
- 95% likely to have a speedup of 1.01x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 0.98x