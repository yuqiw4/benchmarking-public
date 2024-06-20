# Results vs. 3.13.0b2

- fork: brandtbucher
- ref: justin_cache
- machine: linux-x86_64
- commit hash: f4c10d5
- commit date: 2024-04-18
- overall geometric mean: 1.01x slower
- HPT reliability: 99.94%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.09x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240418-linux-x86_64-brandtbucher-justin_cache-3.13.0a6+-f4c10d5 |
|----------------|:----------------------------------------------------------:|:--------------------------------------------------------------------:|
| 2to3           | 274 ms                                                     | 278 ms: 1.02x slower                                                 |
| chameleon      | 7.22 ms                                                    | 7.08 ms: 1.02x faster                                                |
| docutils       | 2.83 sec                                                   | 2.92 sec: 1.03x slower                                               |
| tornado_http   | 94.6 ms                                                    | 96.6 ms: 1.02x slower                                                |
| Geometric mean | (ref)                                                      | 1.01x slower                                                         |

Benchmark hidden because not significant (1): html5lib

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240418-linux-x86_64-brandtbucher-justin_cache-3.13.0a6+-f4c10d5 |
|----------------------------|:----------------------------------------------------------:|:--------------------------------------------------------------------:|
| async_tree_none            | 378 ms                                                     | 362 ms: 1.05x faster                                                 |
| async_tree_cpu_io_mixed_tg | 587 ms                                                     | 609 ms: 1.04x slower                                                 |
| Geometric mean             | (ref)                                                      | 1.01x slower                                                         |

Benchmark hidden because not significant (6): async_tree_memoization_tg, async_tree_io, async_tree_none_tg, async_tree_memoization, async_tree_cpu_io_mixed, async_tree_io_tg

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240418-linux-x86_64-brandtbucher-justin_cache-3.13.0a6+-f4c10d5 |
|----------------|:----------------------------------------------------------:|:--------------------------------------------------------------------:|
| float          | 78.9 ms                                                    | 77.7 ms: 1.01x faster                                                |
| nbody          | 88.3 ms                                                    | 87.3 ms: 1.01x faster                                                |
| pidigits       | 191 ms                                                     | 210 ms: 1.10x slower                                                 |
| Geometric mean | (ref)                                                      | 1.02x slower                                                         |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240418-linux-x86_64-brandtbucher-justin_cache-3.13.0a6+-f4c10d5 |
|----------------|:----------------------------------------------------------:|:--------------------------------------------------------------------:|
| regex_dna      | 221 ms                                                     | 221 ms: 1.00x faster                                                 |
| regex_effbot   | 3.67 ms                                                    | 3.68 ms: 1.00x slower                                                |
| regex_compile  | 137 ms                                                     | 144 ms: 1.05x slower                                                 |
| Geometric mean | (ref)                                                      | 1.01x slower                                                         |

Benchmark hidden because not significant (1): regex_v8

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240418-linux-x86_64-brandtbucher-justin_cache-3.13.0a6+-f4c10d5 |
|----------------------|:----------------------------------------------------------:|:--------------------------------------------------------------------:|
| tomli_loads          | 2.12 sec                                                   | 2.01 sec: 1.05x faster                                               |
| json_loads           | 28.9 us                                                    | 27.7 us: 1.04x faster                                                |
| unpickle_list        | 5.34 us                                                    | 5.27 us: 1.01x faster                                                |
| xml_etree_process    | 61.2 ms                                                    | 60.4 ms: 1.01x faster                                                |
| json_dumps           | 10.7 ms                                                    | 10.6 ms: 1.01x faster                                                |
| xml_etree_generate   | 87.4 ms                                                    | 88.1 ms: 1.01x slower                                                |
| xml_etree_iterparse  | 107 ms                                                     | 109 ms: 1.02x slower                                                 |
| pickle_dict          | 34.8 us                                                    | 36.0 us: 1.04x slower                                                |
| unpickle             | 15.1 us                                                    | 15.7 us: 1.04x slower                                                |
| pickle_list          | 5.11 us                                                    | 5.33 us: 1.04x slower                                                |
| pickle               | 11.5 us                                                    | 12.0 us: 1.05x slower                                                |
| unpickle_pure_python | 218 us                                                     | 236 us: 1.08x slower                                                 |
| Geometric mean       | (ref)                                                      | 1.01x slower                                                         |

Benchmark hidden because not significant (2): xml_etree_parse, pickle_pure_python

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240418-linux-x86_64-brandtbucher-justin_cache-3.13.0a6+-f4c10d5 |
|------------------------|:----------------------------------------------------------:|:--------------------------------------------------------------------:|
| python_startup         | 10.8 ms                                                    | 11.1 ms: 1.04x slower                                                |
| python_startup_no_site | 7.11 ms                                                    | 7.69 ms: 1.08x slower                                                |
| Geometric mean         | (ref)                                                      | 1.06x slower                                                         |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240418-linux-x86_64-brandtbucher-justin_cache-3.13.0a6+-f4c10d5 |
|-----------------|:----------------------------------------------------------:|:--------------------------------------------------------------------:|
| mako            | 11.2 ms                                                    | 11.5 ms: 1.03x slower                                                |
| genshi_text     | 23.7 ms                                                    | 24.4 ms: 1.03x slower                                                |
| django_template | 34.8 ms                                                    | 36.2 ms: 1.04x slower                                                |
| genshi_xml      | 51.6 ms                                                    | 54.9 ms: 1.06x slower                                                |
| Geometric mean  | (ref)                                                      | 1.04x slower                                                         |

All benchmarks:
===============

| Benchmark                  | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240418-linux-x86_64-brandtbucher-justin_cache-3.13.0a6+-f4c10d5 |
|----------------------------|:----------------------------------------------------------:|:--------------------------------------------------------------------:|
| typing_runtime_protocols   | 165 us                                                     | 112 us: 1.47x faster                                                 |
| richards_super             | 57.4 ms                                                    | 49.0 ms: 1.17x faster                                                |
| richards                   | 50.9 ms                                                    | 43.6 ms: 1.17x faster                                                |
| scimark_fft                | 392 ms                                                     | 341 ms: 1.15x faster                                                 |
| scimark_sparse_mat_mult    | 5.27 ms                                                    | 4.83 ms: 1.09x faster                                                |
| mdp                        | 2.79 sec                                                   | 2.64 sec: 1.05x faster                                               |
| tomli_loads                | 2.12 sec                                                   | 2.01 sec: 1.05x faster                                               |
| deepcopy_reduce            | 3.35 us                                                    | 3.19 us: 1.05x faster                                                |
| crypto_pyaes               | 77.5 ms                                                    | 73.9 ms: 1.05x faster                                                |
| async_tree_none            | 378 ms                                                     | 362 ms: 1.05x faster                                                 |
| json                       | 5.31 ms                                                    | 5.09 ms: 1.04x faster                                                |
| json_loads                 | 28.9 us                                                    | 27.7 us: 1.04x faster                                                |
| deepcopy_memo              | 39.7 us                                                    | 38.2 us: 1.04x faster                                                |
| sqlite_synth               | 2.99 us                                                    | 2.88 us: 1.04x faster                                                |
| fannkuch                   | 402 ms                                                     | 389 ms: 1.03x faster                                                 |
| gc_traversal               | 3.98 ms                                                    | 3.85 ms: 1.03x faster                                                |
| deepcopy                   | 367 us                                                     | 356 us: 1.03x faster                                                 |
| create_gc_cycles           | 1.82 ms                                                    | 1.77 ms: 1.03x faster                                                |
| scimark_monte_carlo        | 69.2 ms                                                    | 67.9 ms: 1.02x faster                                                |
| chameleon                  | 7.22 ms                                                    | 7.08 ms: 1.02x faster                                                |
| logging_silent             | 105 ns                                                     | 103 ns: 1.02x faster                                                 |
| logging_format             | 6.47 us                                                    | 6.36 us: 1.02x faster                                                |
| float                      | 78.9 ms                                                    | 77.7 ms: 1.01x faster                                                |
| unpickle_list              | 5.34 us                                                    | 5.27 us: 1.01x faster                                                |
| xml_etree_process          | 61.2 ms                                                    | 60.4 ms: 1.01x faster                                                |
| pprint_pformat             | 1.56 sec                                                   | 1.54 sec: 1.01x faster                                               |
| pyflate                    | 484 ms                                                     | 479 ms: 1.01x faster                                                 |
| nbody                      | 88.3 ms                                                    | 87.3 ms: 1.01x faster                                                |
| pprint_safe_repr           | 758 ms                                                     | 751 ms: 1.01x faster                                                 |
| json_dumps                 | 10.7 ms                                                    | 10.6 ms: 1.01x faster                                                |
| spectral_norm              | 116 ms                                                     | 116 ms: 1.01x faster                                                 |
| regex_dna                  | 221 ms                                                     | 221 ms: 1.00x faster                                                 |
| regex_effbot               | 3.67 ms                                                    | 3.68 ms: 1.00x slower                                                |
| bench_mp_pool              | 23.9 ms                                                    | 24.0 ms: 1.01x slower                                                |
| asyncio_tcp                | 508 ms                                                     | 512 ms: 1.01x slower                                                 |
| xml_etree_generate         | 87.4 ms                                                    | 88.1 ms: 1.01x slower                                                |
| asyncio_tcp_ssl            | 1.84 sec                                                   | 1.86 sec: 1.01x slower                                               |
| sqlglot_parse              | 1.32 ms                                                    | 1.33 ms: 1.01x slower                                                |
| sqlglot_transpile          | 1.63 ms                                                    | 1.65 ms: 1.01x slower                                                |
| dask                       | 369 ms                                                     | 374 ms: 1.01x slower                                                 |
| 2to3                       | 274 ms                                                     | 278 ms: 1.02x slower                                                 |
| xml_etree_iterparse        | 107 ms                                                     | 109 ms: 1.02x slower                                                 |
| telco                      | 8.41 ms                                                    | 8.56 ms: 1.02x slower                                                |
| tornado_http               | 94.6 ms                                                    | 96.6 ms: 1.02x slower                                                |
| go                         | 145 ms                                                     | 148 ms: 1.02x slower                                                 |
| gunicorn                   | 1.28 ms                                                    | 1.31 ms: 1.02x slower                                                |
| djangocms                  | 31.5 us                                                    | 32.2 us: 1.02x slower                                                |
| meteor_contest             | 110 ms                                                     | 113 ms: 1.02x slower                                                 |
| mako                       | 11.2 ms                                                    | 11.5 ms: 1.03x slower                                                |
| aiohttp                    | 1.18 ms                                                    | 1.21 ms: 1.03x slower                                                |
| generators                 | 29.6 ms                                                    | 30.5 ms: 1.03x slower                                                |
| pathlib                    | 17.3 ms                                                    | 17.8 ms: 1.03x slower                                                |
| sqlglot_normalize          | 110 ms                                                     | 114 ms: 1.03x slower                                                 |
| chaos                      | 61.3 ms                                                    | 63.3 ms: 1.03x slower                                                |
| genshi_text                | 23.7 ms                                                    | 24.4 ms: 1.03x slower                                                |
| raytrace                   | 267 ms                                                     | 275 ms: 1.03x slower                                                 |
| docutils                   | 2.83 sec                                                   | 2.92 sec: 1.03x slower                                               |
| bench_thread_pool          | 834 us                                                     | 863 us: 1.04x slower                                                 |
| python_startup             | 10.8 ms                                                    | 11.1 ms: 1.04x slower                                                |
| pickle_dict                | 34.8 us                                                    | 36.0 us: 1.04x slower                                                |
| async_tree_cpu_io_mixed_tg | 587 ms                                                     | 609 ms: 1.04x slower                                                 |
| scimark_sor                | 127 ms                                                     | 132 ms: 1.04x slower                                                 |
| django_template            | 34.8 ms                                                    | 36.2 ms: 1.04x slower                                                |
| sqlglot_optimize           | 55.5 ms                                                    | 57.8 ms: 1.04x slower                                                |
| dulwich_log                | 67.2 ms                                                    | 69.9 ms: 1.04x slower                                                |
| unpickle                   | 15.1 us                                                    | 15.7 us: 1.04x slower                                                |
| async_generators           | 442 ms                                                     | 460 ms: 1.04x slower                                                 |
| pickle_list                | 5.11 us                                                    | 5.33 us: 1.04x slower                                                |
| pickle                     | 11.5 us                                                    | 12.0 us: 1.05x slower                                                |
| regex_compile              | 137 ms                                                     | 144 ms: 1.05x slower                                                 |
| coverage                   | 93.1 ms                                                    | 98.2 ms: 1.05x slower                                                |
| mypy2                      | 742 ms                                                     | 782 ms: 1.05x slower                                                 |
| sympy_expand               | 473 ms                                                     | 501 ms: 1.06x slower                                                 |
| sympy_str                  | 282 ms                                                     | 299 ms: 1.06x slower                                                 |
| genshi_xml                 | 51.6 ms                                                    | 54.9 ms: 1.06x slower                                                |
| sympy_integrate            | 20.5 ms                                                    | 22.1 ms: 1.08x slower                                                |
| unpickle_pure_python       | 218 us                                                     | 236 us: 1.08x slower                                                 |
| python_startup_no_site     | 7.11 ms                                                    | 7.69 ms: 1.08x slower                                                |
| sympy_sum                  | 156 ms                                                     | 170 ms: 1.09x slower                                                 |
| pidigits                   | 191 ms                                                     | 210 ms: 1.10x slower                                                 |
| comprehensions             | 16.6 us                                                    | 18.3 us: 1.10x slower                                                |
| scimark_lu                 | 122 ms                                                     | 134 ms: 1.10x slower                                                 |
| hexiom                     | 6.30 ms                                                    | 7.09 ms: 1.13x slower                                                |
| deltablue                  | 3.25 ms                                                    | 3.69 ms: 1.13x slower                                                |
| nqueens                    | 81.4 ms                                                    | 93.0 ms: 1.14x slower                                                |
| Geometric mean             | (ref)                                                      | 1.01x slower                                                         |

Benchmark hidden because not significant (16): xml_etree_parse, coroutines, regex_v8, thrift, pickle_pure_python, async_tree_memoization_tg, logging_simple, asyncio_websockets, html5lib, async_tree_io, async_tree_none_tg, pycparser, async_tree_memoization, async_tree_cpu_io_mixed, async_tree_io_tg, pylint
Ignored benchmarks (2) of results/bm-20240605-3.13.0b2-3a83b17/bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17.json: bpe_tokeniser, flaskblogging

# HPT report

- Reliability score: 99.94% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.09x