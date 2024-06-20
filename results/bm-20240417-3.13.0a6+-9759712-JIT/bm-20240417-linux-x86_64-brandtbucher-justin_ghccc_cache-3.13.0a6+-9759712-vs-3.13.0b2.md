# Results vs. 3.13.0b2

- fork: brandtbucher
- ref: justin_ghccc_cache
- machine: linux-x86_64
- commit hash: 9759712
- commit date: 2024-04-17
- overall geometric mean: 1.01x faster
- HPT reliability: 87.00%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.09x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240417-linux-x86_64-brandtbucher-justin_ghccc_cache-3.13.0a6+-9759712 |
|----------------|:----------------------------------------------------------:|:--------------------------------------------------------------------------:|
| 2to3           | 274 ms                                                     | 276 ms: 1.01x slower                                                       |
| chameleon      | 7.22 ms                                                    | 7.12 ms: 1.01x faster                                                      |
| docutils       | 2.83 sec                                                   | 2.91 sec: 1.03x slower                                                     |
| html5lib       | 67.2 ms                                                    | 67.9 ms: 1.01x slower                                                      |
| tornado_http   | 94.6 ms                                                    | 96.2 ms: 1.02x slower                                                      |
| Geometric mean | (ref)                                                      | 1.01x slower                                                               |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240417-linux-x86_64-brandtbucher-justin_ghccc_cache-3.13.0a6+-9759712 |
|----------------------------|:----------------------------------------------------------:|:--------------------------------------------------------------------------:|
| async_tree_none            | 378 ms                                                     | 357 ms: 1.06x faster                                                       |
| async_tree_cpu_io_mixed_tg | 587 ms                                                     | 610 ms: 1.04x slower                                                       |
| Geometric mean             | (ref)                                                      | 1.00x faster                                                               |

Benchmark hidden because not significant (6): async_tree_io, async_tree_memoization_tg, async_tree_none_tg, async_tree_cpu_io_mixed, async_tree_memoization, async_tree_io_tg

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240417-linux-x86_64-brandtbucher-justin_ghccc_cache-3.13.0a6+-9759712 |
|----------------|:----------------------------------------------------------:|:--------------------------------------------------------------------------:|
| nbody          | 88.3 ms                                                    | 77.1 ms: 1.14x faster                                                      |
| float          | 78.9 ms                                                    | 72.9 ms: 1.08x faster                                                      |
| pidigits       | 191 ms                                                     | 189 ms: 1.01x faster                                                       |
| Geometric mean | (ref)                                                      | 1.08x faster                                                               |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240417-linux-x86_64-brandtbucher-justin_ghccc_cache-3.13.0a6+-9759712 |
|----------------|:----------------------------------------------------------:|:--------------------------------------------------------------------------:|
| regex_dna      | 221 ms                                                     | 225 ms: 1.02x slower                                                       |
| regex_compile  | 137 ms                                                     | 140 ms: 1.02x slower                                                       |
| regex_v8       | 25.1 ms                                                    | 25.8 ms: 1.03x slower                                                      |
| regex_effbot   | 3.67 ms                                                    | 3.77 ms: 1.03x slower                                                      |
| Geometric mean | (ref)                                                      | 1.02x slower                                                               |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240417-linux-x86_64-brandtbucher-justin_ghccc_cache-3.13.0a6+-9759712 |
|----------------------|:----------------------------------------------------------:|:--------------------------------------------------------------------------:|
| tomli_loads          | 2.12 sec                                                   | 1.93 sec: 1.10x faster                                                     |
| unpickle_list        | 5.34 us                                                    | 5.12 us: 1.04x faster                                                      |
| pickle_list          | 5.11 us                                                    | 4.91 us: 1.04x faster                                                      |
| json_loads           | 28.9 us                                                    | 27.8 us: 1.04x faster                                                      |
| xml_etree_process    | 61.2 ms                                                    | 59.5 ms: 1.03x faster                                                      |
| json_dumps           | 10.7 ms                                                    | 10.5 ms: 1.02x faster                                                      |
| pickle_dict          | 34.8 us                                                    | 34.1 us: 1.02x faster                                                      |
| xml_etree_iterparse  | 107 ms                                                     | 106 ms: 1.01x faster                                                       |
| pickle_pure_python   | 305 us                                                     | 304 us: 1.00x faster                                                       |
| pickle               | 11.5 us                                                    | 11.6 us: 1.01x slower                                                      |
| unpickle             | 15.1 us                                                    | 15.3 us: 1.01x slower                                                      |
| unpickle_pure_python | 218 us                                                     | 224 us: 1.03x slower                                                       |
| Geometric mean       | (ref)                                                      | 1.02x faster                                                               |

Benchmark hidden because not significant (2): xml_etree_parse, xml_etree_generate

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240417-linux-x86_64-brandtbucher-justin_ghccc_cache-3.13.0a6+-9759712 |
|------------------------|:----------------------------------------------------------:|:--------------------------------------------------------------------------:|
| python_startup         | 10.8 ms                                                    | 11.1 ms: 1.03x slower                                                      |
| python_startup_no_site | 7.11 ms                                                    | 7.66 ms: 1.08x slower                                                      |
| Geometric mean         | (ref)                                                      | 1.06x slower                                                               |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240417-linux-x86_64-brandtbucher-justin_ghccc_cache-3.13.0a6+-9759712 |
|-----------------|:----------------------------------------------------------:|:--------------------------------------------------------------------------:|
| mako            | 11.2 ms                                                    | 10.1 ms: 1.11x faster                                                      |
| genshi_text     | 23.7 ms                                                    | 23.9 ms: 1.01x slower                                                      |
| django_template | 34.8 ms                                                    | 35.6 ms: 1.02x slower                                                      |
| genshi_xml      | 51.6 ms                                                    | 54.2 ms: 1.05x slower                                                      |
| Geometric mean  | (ref)                                                      | 1.01x faster                                                               |

All benchmarks:
===============

| Benchmark                  | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240417-linux-x86_64-brandtbucher-justin_ghccc_cache-3.13.0a6+-9759712 |
|----------------------------|:----------------------------------------------------------:|:--------------------------------------------------------------------------:|
| typing_runtime_protocols   | 165 us                                                     | 112 us: 1.47x faster                                                       |
| scimark_fft                | 392 ms                                                     | 304 ms: 1.29x faster                                                       |
| scimark_sparse_mat_mult    | 5.27 ms                                                    | 4.34 ms: 1.21x faster                                                      |
| richards                   | 50.9 ms                                                    | 42.9 ms: 1.19x faster                                                      |
| richards_super             | 57.4 ms                                                    | 48.5 ms: 1.18x faster                                                      |
| spectral_norm              | 116 ms                                                     | 99.8 ms: 1.16x faster                                                      |
| fannkuch                   | 402 ms                                                     | 350 ms: 1.15x faster                                                       |
| nbody                      | 88.3 ms                                                    | 77.1 ms: 1.14x faster                                                      |
| crypto_pyaes               | 77.5 ms                                                    | 68.5 ms: 1.13x faster                                                      |
| mako                       | 11.2 ms                                                    | 10.1 ms: 1.11x faster                                                      |
| tomli_loads                | 2.12 sec                                                   | 1.93 sec: 1.10x faster                                                     |
| pyflate                    | 484 ms                                                     | 441 ms: 1.10x faster                                                       |
| scimark_monte_carlo        | 69.2 ms                                                    | 63.4 ms: 1.09x faster                                                      |
| float                      | 78.9 ms                                                    | 72.9 ms: 1.08x faster                                                      |
| async_tree_none            | 378 ms                                                     | 357 ms: 1.06x faster                                                       |
| pprint_pformat             | 1.56 sec                                                   | 1.48 sec: 1.05x faster                                                     |
| pprint_safe_repr           | 758 ms                                                     | 722 ms: 1.05x faster                                                       |
| deepcopy_reduce            | 3.35 us                                                    | 3.19 us: 1.05x faster                                                      |
| json                       | 5.31 ms                                                    | 5.08 ms: 1.04x faster                                                      |
| unpickle_list              | 5.34 us                                                    | 5.12 us: 1.04x faster                                                      |
| sqlite_synth               | 2.99 us                                                    | 2.87 us: 1.04x faster                                                      |
| pickle_list                | 5.11 us                                                    | 4.91 us: 1.04x faster                                                      |
| json_loads                 | 28.9 us                                                    | 27.8 us: 1.04x faster                                                      |
| create_gc_cycles           | 1.82 ms                                                    | 1.75 ms: 1.04x faster                                                      |
| xml_etree_process          | 61.2 ms                                                    | 59.5 ms: 1.03x faster                                                      |
| deepcopy                   | 367 us                                                     | 359 us: 1.02x faster                                                       |
| json_dumps                 | 10.7 ms                                                    | 10.5 ms: 1.02x faster                                                      |
| coroutines                 | 23.2 ms                                                    | 22.7 ms: 1.02x faster                                                      |
| pickle_dict                | 34.8 us                                                    | 34.1 us: 1.02x faster                                                      |
| chaos                      | 61.3 ms                                                    | 60.2 ms: 1.02x faster                                                      |
| logging_silent             | 105 ns                                                     | 103 ns: 1.02x faster                                                       |
| logging_format             | 6.47 us                                                    | 6.37 us: 1.02x faster                                                      |
| pidigits                   | 191 ms                                                     | 189 ms: 1.01x faster                                                       |
| chameleon                  | 7.22 ms                                                    | 7.12 ms: 1.01x faster                                                      |
| scimark_sor                | 127 ms                                                     | 126 ms: 1.01x faster                                                       |
| mdp                        | 2.79 sec                                                   | 2.75 sec: 1.01x faster                                                     |
| deepcopy_memo              | 39.7 us                                                    | 39.3 us: 1.01x faster                                                      |
| xml_etree_iterparse        | 107 ms                                                     | 106 ms: 1.01x faster                                                       |
| sqlglot_parse              | 1.32 ms                                                    | 1.31 ms: 1.01x faster                                                      |
| meteor_contest             | 110 ms                                                     | 109 ms: 1.01x faster                                                       |
| sqlglot_transpile          | 1.63 ms                                                    | 1.63 ms: 1.00x faster                                                      |
| asyncio_websockets         | 567 ms                                                     | 564 ms: 1.00x faster                                                       |
| pickle_pure_python         | 305 us                                                     | 304 us: 1.00x faster                                                       |
| 2to3                       | 274 ms                                                     | 276 ms: 1.01x slower                                                       |
| asyncio_tcp                | 508 ms                                                     | 512 ms: 1.01x slower                                                       |
| gc_traversal               | 3.98 ms                                                    | 4.00 ms: 1.01x slower                                                      |
| bench_mp_pool              | 23.9 ms                                                    | 24.1 ms: 1.01x slower                                                      |
| asyncio_tcp_ssl            | 1.84 sec                                                   | 1.86 sec: 1.01x slower                                                     |
| pickle                     | 11.5 us                                                    | 11.6 us: 1.01x slower                                                      |
| html5lib                   | 67.2 ms                                                    | 67.9 ms: 1.01x slower                                                      |
| genshi_text                | 23.7 ms                                                    | 23.9 ms: 1.01x slower                                                      |
| unpickle                   | 15.1 us                                                    | 15.3 us: 1.01x slower                                                      |
| raytrace                   | 267 ms                                                     | 270 ms: 1.01x slower                                                       |
| telco                      | 8.41 ms                                                    | 8.52 ms: 1.01x slower                                                      |
| dask                       | 369 ms                                                     | 375 ms: 1.01x slower                                                       |
| pathlib                    | 17.3 ms                                                    | 17.6 ms: 1.01x slower                                                      |
| go                         | 145 ms                                                     | 147 ms: 1.02x slower                                                       |
| regex_dna                  | 221 ms                                                     | 225 ms: 1.02x slower                                                       |
| tornado_http               | 94.6 ms                                                    | 96.2 ms: 1.02x slower                                                      |
| scimark_lu                 | 122 ms                                                     | 124 ms: 1.02x slower                                                       |
| gunicorn                   | 1.28 ms                                                    | 1.30 ms: 1.02x slower                                                      |
| regex_compile              | 137 ms                                                     | 140 ms: 1.02x slower                                                       |
| django_template            | 34.8 ms                                                    | 35.6 ms: 1.02x slower                                                      |
| sqlglot_normalize          | 110 ms                                                     | 113 ms: 1.02x slower                                                       |
| aiohttp                    | 1.18 ms                                                    | 1.21 ms: 1.03x slower                                                      |
| regex_v8                   | 25.1 ms                                                    | 25.8 ms: 1.03x slower                                                      |
| unpickle_pure_python       | 218 us                                                     | 224 us: 1.03x slower                                                       |
| regex_effbot               | 3.67 ms                                                    | 3.77 ms: 1.03x slower                                                      |
| dulwich_log                | 67.2 ms                                                    | 69.1 ms: 1.03x slower                                                      |
| docutils                   | 2.83 sec                                                   | 2.91 sec: 1.03x slower                                                     |
| python_startup             | 10.8 ms                                                    | 11.1 ms: 1.03x slower                                                      |
| sqlglot_optimize           | 55.5 ms                                                    | 57.3 ms: 1.03x slower                                                      |
| comprehensions             | 16.6 us                                                    | 17.2 us: 1.03x slower                                                      |
| bench_thread_pool          | 834 us                                                     | 864 us: 1.04x slower                                                       |
| async_tree_cpu_io_mixed_tg | 587 ms                                                     | 610 ms: 1.04x slower                                                       |
| sympy_str                  | 282 ms                                                     | 295 ms: 1.04x slower                                                       |
| pycparser                  | 1.16 sec                                                   | 1.22 sec: 1.05x slower                                                     |
| genshi_xml                 | 51.6 ms                                                    | 54.2 ms: 1.05x slower                                                      |
| sympy_expand               | 473 ms                                                     | 496 ms: 1.05x slower                                                       |
| coverage                   | 93.1 ms                                                    | 97.8 ms: 1.05x slower                                                      |
| mypy2                      | 742 ms                                                     | 782 ms: 1.05x slower                                                       |
| hexiom                     | 6.30 ms                                                    | 6.71 ms: 1.07x slower                                                      |
| async_generators           | 442 ms                                                     | 471 ms: 1.07x slower                                                       |
| sympy_integrate            | 20.5 ms                                                    | 22.0 ms: 1.07x slower                                                      |
| python_startup_no_site     | 7.11 ms                                                    | 7.66 ms: 1.08x slower                                                      |
| sympy_sum                  | 156 ms                                                     | 168 ms: 1.08x slower                                                       |
| nqueens                    | 81.4 ms                                                    | 88.2 ms: 1.08x slower                                                      |
| deltablue                  | 3.25 ms                                                    | 3.67 ms: 1.13x slower                                                      |
| Geometric mean             | (ref)                                                      | 1.01x faster                                                               |

Benchmark hidden because not significant (13): async_tree_io, async_tree_memoization_tg, xml_etree_parse, xml_etree_generate, async_tree_none_tg, logging_simple, djangocms, generators, thrift, async_tree_cpu_io_mixed, async_tree_memoization, async_tree_io_tg, pylint
Ignored benchmarks (2) of results/bm-20240605-3.13.0b2-3a83b17/bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17.json: bpe_tokeniser, flaskblogging

# HPT report

- Reliability score: 87.00% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.09x