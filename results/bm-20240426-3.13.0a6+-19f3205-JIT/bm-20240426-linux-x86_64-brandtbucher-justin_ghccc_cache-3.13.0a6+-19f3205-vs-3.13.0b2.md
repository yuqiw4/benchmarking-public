# Results vs. 3.13.0b2

- fork: brandtbucher
- ref: justin_ghccc_cache
- machine: linux-x86_64
- commit hash: 19f3205
- commit date: 2024-04-26
- overall geometric mean: 1.01x faster
- HPT reliability: 92.81%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.09x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240426-linux-x86_64-brandtbucher-justin_ghccc_cache-3.13.0a6+-19f3205 |
|----------------|:----------------------------------------------------------:|:--------------------------------------------------------------------------:|
| 2to3           | 274 ms                                                     | 276 ms: 1.01x slower                                                       |
| chameleon      | 7.22 ms                                                    | 6.99 ms: 1.03x faster                                                      |
| docutils       | 2.83 sec                                                   | 2.92 sec: 1.03x slower                                                     |
| html5lib       | 67.2 ms                                                    | 68.5 ms: 1.02x slower                                                      |
| tornado_http   | 94.6 ms                                                    | 96.2 ms: 1.02x slower                                                      |
| Geometric mean | (ref)                                                      | 1.01x slower                                                               |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240426-linux-x86_64-brandtbucher-justin_ghccc_cache-3.13.0a6+-19f3205 |
|----------------------------|:----------------------------------------------------------:|:--------------------------------------------------------------------------:|
| async_tree_none            | 378 ms                                                     | 355 ms: 1.07x faster                                                       |
| async_tree_cpu_io_mixed_tg | 587 ms                                                     | 608 ms: 1.03x slower                                                       |
| Geometric mean             | (ref)                                                      | 1.01x faster                                                               |

Benchmark hidden because not significant (6): async_tree_io, async_tree_memoization_tg, async_tree_memoization, async_tree_none_tg, async_tree_cpu_io_mixed, async_tree_io_tg

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240426-linux-x86_64-brandtbucher-justin_ghccc_cache-3.13.0a6+-19f3205 |
|----------------|:----------------------------------------------------------:|:--------------------------------------------------------------------------:|
| nbody          | 88.3 ms                                                    | 77.8 ms: 1.13x faster                                                      |
| float          | 78.9 ms                                                    | 72.7 ms: 1.08x faster                                                      |
| pidigits       | 191 ms                                                     | 190 ms: 1.01x faster                                                       |
| Geometric mean | (ref)                                                      | 1.07x faster                                                               |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240426-linux-x86_64-brandtbucher-justin_ghccc_cache-3.13.0a6+-19f3205 |
|----------------|:----------------------------------------------------------:|:--------------------------------------------------------------------------:|
| regex_v8       | 25.1 ms                                                    | 25.3 ms: 1.01x slower                                                      |
| regex_compile  | 137 ms                                                     | 139 ms: 1.01x slower                                                       |
| regex_effbot   | 3.67 ms                                                    | 3.73 ms: 1.02x slower                                                      |
| regex_dna      | 221 ms                                                     | 230 ms: 1.04x slower                                                       |
| Geometric mean | (ref)                                                      | 1.02x slower                                                               |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240426-linux-x86_64-brandtbucher-justin_ghccc_cache-3.13.0a6+-19f3205 |
|----------------------|:----------------------------------------------------------:|:--------------------------------------------------------------------------:|
| tomli_loads          | 2.12 sec                                                   | 1.92 sec: 1.10x faster                                                     |
| xml_etree_parse      | 162 ms                                                     | 149 ms: 1.09x faster                                                       |
| xml_etree_iterparse  | 107 ms                                                     | 102 ms: 1.05x faster                                                       |
| json_loads           | 28.9 us                                                    | 27.6 us: 1.05x faster                                                      |
| unpickle_list        | 5.34 us                                                    | 5.26 us: 1.02x faster                                                      |
| xml_etree_process    | 61.2 ms                                                    | 60.3 ms: 1.02x faster                                                      |
| unpickle             | 15.1 us                                                    | 15.0 us: 1.01x faster                                                      |
| pickle               | 11.5 us                                                    | 11.7 us: 1.02x slower                                                      |
| pickle_dict          | 34.8 us                                                    | 35.4 us: 1.02x slower                                                      |
| unpickle_pure_python | 218 us                                                     | 226 us: 1.04x slower                                                       |
| Geometric mean       | (ref)                                                      | 1.02x faster                                                               |

Benchmark hidden because not significant (4): json_dumps, pickle_pure_python, xml_etree_generate, pickle_list

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240426-linux-x86_64-brandtbucher-justin_ghccc_cache-3.13.0a6+-19f3205 |
|------------------------|:----------------------------------------------------------:|:--------------------------------------------------------------------------:|
| python_startup         | 10.8 ms                                                    | 11.1 ms: 1.03x slower                                                      |
| python_startup_no_site | 7.11 ms                                                    | 7.69 ms: 1.08x slower                                                      |
| Geometric mean         | (ref)                                                      | 1.06x slower                                                               |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240426-linux-x86_64-brandtbucher-justin_ghccc_cache-3.13.0a6+-19f3205 |
|-----------------|:----------------------------------------------------------:|:--------------------------------------------------------------------------:|
| mako            | 11.2 ms                                                    | 10.1 ms: 1.12x faster                                                      |
| django_template | 34.8 ms                                                    | 35.8 ms: 1.03x slower                                                      |
| genshi_text     | 23.7 ms                                                    | 24.4 ms: 1.03x slower                                                      |
| genshi_xml      | 51.6 ms                                                    | 53.9 ms: 1.04x slower                                                      |
| Geometric mean  | (ref)                                                      | 1.00x faster                                                               |

All benchmarks:
===============

| Benchmark                  | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240426-linux-x86_64-brandtbucher-justin_ghccc_cache-3.13.0a6+-19f3205 |
|----------------------------|:----------------------------------------------------------:|:--------------------------------------------------------------------------:|
| typing_runtime_protocols   | 165 us                                                     | 117 us: 1.41x faster                                                       |
| scimark_fft                | 392 ms                                                     | 303 ms: 1.29x faster                                                       |
| scimark_sparse_mat_mult    | 5.27 ms                                                    | 4.33 ms: 1.22x faster                                                      |
| richards                   | 50.9 ms                                                    | 41.9 ms: 1.21x faster                                                      |
| spectral_norm              | 116 ms                                                     | 97.9 ms: 1.19x faster                                                      |
| richards_super             | 57.4 ms                                                    | 48.4 ms: 1.19x faster                                                      |
| fannkuch                   | 402 ms                                                     | 353 ms: 1.14x faster                                                       |
| crypto_pyaes               | 77.5 ms                                                    | 68.3 ms: 1.13x faster                                                      |
| nbody                      | 88.3 ms                                                    | 77.8 ms: 1.13x faster                                                      |
| mako                       | 11.2 ms                                                    | 10.1 ms: 1.12x faster                                                      |
| tomli_loads                | 2.12 sec                                                   | 1.92 sec: 1.10x faster                                                     |
| xml_etree_parse            | 162 ms                                                     | 149 ms: 1.09x faster                                                       |
| scimark_monte_carlo        | 69.2 ms                                                    | 63.6 ms: 1.09x faster                                                      |
| float                      | 78.9 ms                                                    | 72.7 ms: 1.08x faster                                                      |
| pyflate                    | 484 ms                                                     | 448 ms: 1.08x faster                                                       |
| async_tree_none            | 378 ms                                                     | 355 ms: 1.07x faster                                                       |
| pprint_pformat             | 1.56 sec                                                   | 1.47 sec: 1.06x faster                                                     |
| xml_etree_iterparse        | 107 ms                                                     | 102 ms: 1.05x faster                                                       |
| json                       | 5.31 ms                                                    | 5.04 ms: 1.05x faster                                                      |
| sqlite_synth               | 2.99 us                                                    | 2.85 us: 1.05x faster                                                      |
| json_loads                 | 28.9 us                                                    | 27.6 us: 1.05x faster                                                      |
| deepcopy_reduce            | 3.35 us                                                    | 3.21 us: 1.04x faster                                                      |
| pprint_safe_repr           | 758 ms                                                     | 728 ms: 1.04x faster                                                       |
| chameleon                  | 7.22 ms                                                    | 6.99 ms: 1.03x faster                                                      |
| create_gc_cycles           | 1.82 ms                                                    | 1.77 ms: 1.03x faster                                                      |
| gc_traversal               | 3.98 ms                                                    | 3.87 ms: 1.03x faster                                                      |
| logging_silent             | 105 ns                                                     | 103 ns: 1.02x faster                                                       |
| chaos                      | 61.3 ms                                                    | 60.3 ms: 1.02x faster                                                      |
| unpickle_list              | 5.34 us                                                    | 5.26 us: 1.02x faster                                                      |
| deepcopy                   | 367 us                                                     | 362 us: 1.02x faster                                                       |
| xml_etree_process          | 61.2 ms                                                    | 60.3 ms: 1.02x faster                                                      |
| deepcopy_memo              | 39.7 us                                                    | 39.1 us: 1.01x faster                                                      |
| coroutines                 | 23.2 ms                                                    | 22.9 ms: 1.01x faster                                                      |
| unpickle                   | 15.1 us                                                    | 15.0 us: 1.01x faster                                                      |
| pidigits                   | 191 ms                                                     | 190 ms: 1.01x faster                                                       |
| mdp                        | 2.79 sec                                                   | 2.77 sec: 1.01x faster                                                     |
| asyncio_websockets         | 567 ms                                                     | 564 ms: 1.01x faster                                                       |
| asyncio_tcp_ssl            | 1.84 sec                                                   | 1.85 sec: 1.01x slower                                                     |
| 2to3                       | 274 ms                                                     | 276 ms: 1.01x slower                                                       |
| regex_v8                   | 25.1 ms                                                    | 25.3 ms: 1.01x slower                                                      |
| logging_simple             | 5.74 us                                                    | 5.80 us: 1.01x slower                                                      |
| bench_mp_pool              | 23.9 ms                                                    | 24.1 ms: 1.01x slower                                                      |
| meteor_contest             | 110 ms                                                     | 111 ms: 1.01x slower                                                       |
| regex_compile              | 137 ms                                                     | 139 ms: 1.01x slower                                                       |
| asyncio_tcp                | 508 ms                                                     | 516 ms: 1.02x slower                                                       |
| regex_effbot               | 3.67 ms                                                    | 3.73 ms: 1.02x slower                                                      |
| tornado_http               | 94.6 ms                                                    | 96.2 ms: 1.02x slower                                                      |
| pickle                     | 11.5 us                                                    | 11.7 us: 1.02x slower                                                      |
| scimark_sor                | 127 ms                                                     | 130 ms: 1.02x slower                                                       |
| gunicorn                   | 1.28 ms                                                    | 1.30 ms: 1.02x slower                                                      |
| pickle_dict                | 34.8 us                                                    | 35.4 us: 1.02x slower                                                      |
| html5lib                   | 67.2 ms                                                    | 68.5 ms: 1.02x slower                                                      |
| generators                 | 29.6 ms                                                    | 30.3 ms: 1.02x slower                                                      |
| pathlib                    | 17.3 ms                                                    | 17.7 ms: 1.02x slower                                                      |
| raytrace                   | 267 ms                                                     | 273 ms: 1.02x slower                                                       |
| aiohttp                    | 1.18 ms                                                    | 1.21 ms: 1.02x slower                                                      |
| telco                      | 8.41 ms                                                    | 8.63 ms: 1.03x slower                                                      |
| django_template            | 34.8 ms                                                    | 35.8 ms: 1.03x slower                                                      |
| sqlglot_optimize           | 55.5 ms                                                    | 57.1 ms: 1.03x slower                                                      |
| sqlglot_normalize          | 110 ms                                                     | 113 ms: 1.03x slower                                                       |
| genshi_text                | 23.7 ms                                                    | 24.4 ms: 1.03x slower                                                      |
| dulwich_log                | 67.2 ms                                                    | 69.2 ms: 1.03x slower                                                      |
| docutils                   | 2.83 sec                                                   | 2.92 sec: 1.03x slower                                                     |
| go                         | 145 ms                                                     | 149 ms: 1.03x slower                                                       |
| comprehensions             | 16.6 us                                                    | 17.2 us: 1.03x slower                                                      |
| djangocms                  | 31.5 us                                                    | 32.6 us: 1.03x slower                                                      |
| async_tree_cpu_io_mixed_tg | 587 ms                                                     | 608 ms: 1.03x slower                                                       |
| python_startup             | 10.8 ms                                                    | 11.1 ms: 1.03x slower                                                      |
| unpickle_pure_python       | 218 us                                                     | 226 us: 1.04x slower                                                       |
| hexiom                     | 6.30 ms                                                    | 6.53 ms: 1.04x slower                                                      |
| bench_thread_pool          | 834 us                                                     | 866 us: 1.04x slower                                                       |
| regex_dna                  | 221 ms                                                     | 230 ms: 1.04x slower                                                       |
| sympy_str                  | 282 ms                                                     | 294 ms: 1.04x slower                                                       |
| scimark_lu                 | 122 ms                                                     | 127 ms: 1.04x slower                                                       |
| genshi_xml                 | 51.6 ms                                                    | 53.9 ms: 1.04x slower                                                      |
| coverage                   | 93.1 ms                                                    | 97.4 ms: 1.05x slower                                                      |
| sympy_expand               | 473 ms                                                     | 497 ms: 1.05x slower                                                       |
| nqueens                    | 81.4 ms                                                    | 85.7 ms: 1.05x slower                                                      |
| async_generators           | 442 ms                                                     | 467 ms: 1.06x slower                                                       |
| mypy2                      | 742 ms                                                     | 787 ms: 1.06x slower                                                       |
| sympy_sum                  | 156 ms                                                     | 167 ms: 1.07x slower                                                       |
| sympy_integrate            | 20.5 ms                                                    | 22.0 ms: 1.07x slower                                                      |
| python_startup_no_site     | 7.11 ms                                                    | 7.69 ms: 1.08x slower                                                      |
| deltablue                  | 3.25 ms                                                    | 3.67 ms: 1.13x slower                                                      |
| Geometric mean             | (ref)                                                      | 1.01x faster                                                               |

Benchmark hidden because not significant (17): async_tree_io, async_tree_memoization_tg, async_tree_memoization, json_dumps, async_tree_none_tg, logging_format, pickle_pure_python, xml_etree_generate, pickle_list, sqlglot_transpile, thrift, sqlglot_parse, async_tree_cpu_io_mixed, async_tree_io_tg, pycparser, dask, pylint
Ignored benchmarks (2) of results/bm-20240605-3.13.0b2-3a83b17/bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17.json: bpe_tokeniser, flaskblogging

# HPT report

- Reliability score: 92.81% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.09x