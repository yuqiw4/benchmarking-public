# Results vs. 3.13.0b2

- fork: brandtbucher
- ref: justin_ghccc_cache
- machine: linux-x86_64
- commit hash: 280cb86
- commit date: 2024-04-25
- overall geometric mean: 1.02x faster
- HPT reliability: 82.90%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.09x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240425-linux-x86_64-brandtbucher-justin_ghccc_cache-3.13.0a6+-280cb86 |
|----------------|:----------------------------------------------------------:|:--------------------------------------------------------------------------:|
| 2to3           | 274 ms                                                     | 275 ms: 1.00x slower                                                       |
| chameleon      | 7.22 ms                                                    | 6.94 ms: 1.04x faster                                                      |
| docutils       | 2.83 sec                                                   | 2.92 sec: 1.03x slower                                                     |
| html5lib       | 67.2 ms                                                    | 68.2 ms: 1.01x slower                                                      |
| tornado_http   | 94.6 ms                                                    | 95.3 ms: 1.01x slower                                                      |
| Geometric mean | (ref)                                                      | 1.00x slower                                                               |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240425-linux-x86_64-brandtbucher-justin_ghccc_cache-3.13.0a6+-280cb86 |
|----------------------------|:----------------------------------------------------------:|:--------------------------------------------------------------------------:|
| async_tree_none            | 378 ms                                                     | 356 ms: 1.06x faster                                                       |
| async_tree_cpu_io_mixed_tg | 587 ms                                                     | 605 ms: 1.03x slower                                                       |
| Geometric mean             | (ref)                                                      | 1.00x faster                                                               |

Benchmark hidden because not significant (6): async_tree_memoization_tg, async_tree_memoization, async_tree_io, async_tree_none_tg, async_tree_cpu_io_mixed, async_tree_io_tg

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240425-linux-x86_64-brandtbucher-justin_ghccc_cache-3.13.0a6+-280cb86 |
|----------------|:----------------------------------------------------------:|:--------------------------------------------------------------------------:|
| nbody          | 88.3 ms                                                    | 75.3 ms: 1.17x faster                                                      |
| float          | 78.9 ms                                                    | 72.6 ms: 1.09x faster                                                      |
| pidigits       | 191 ms                                                     | 193 ms: 1.01x slower                                                       |
| Geometric mean | (ref)                                                      | 1.08x faster                                                               |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240425-linux-x86_64-brandtbucher-justin_ghccc_cache-3.13.0a6+-280cb86 |
|----------------|:----------------------------------------------------------:|:--------------------------------------------------------------------------:|
| regex_v8       | 25.1 ms                                                    | 25.5 ms: 1.01x slower                                                      |
| regex_compile  | 137 ms                                                     | 140 ms: 1.02x slower                                                       |
| regex_effbot   | 3.67 ms                                                    | 3.76 ms: 1.02x slower                                                      |
| regex_dna      | 221 ms                                                     | 230 ms: 1.04x slower                                                       |
| Geometric mean | (ref)                                                      | 1.02x slower                                                               |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240425-linux-x86_64-brandtbucher-justin_ghccc_cache-3.13.0a6+-280cb86 |
|----------------------|:----------------------------------------------------------:|:--------------------------------------------------------------------------:|
| tomli_loads          | 2.12 sec                                                   | 1.90 sec: 1.12x faster                                                     |
| xml_etree_parse      | 162 ms                                                     | 148 ms: 1.09x faster                                                       |
| xml_etree_iterparse  | 107 ms                                                     | 102 ms: 1.05x faster                                                       |
| json_loads           | 28.9 us                                                    | 27.6 us: 1.05x faster                                                      |
| unpickle_list        | 5.34 us                                                    | 5.14 us: 1.04x faster                                                      |
| xml_etree_process    | 61.2 ms                                                    | 59.7 ms: 1.02x faster                                                      |
| json_dumps           | 10.7 ms                                                    | 10.6 ms: 1.01x faster                                                      |
| xml_etree_generate   | 87.4 ms                                                    | 86.7 ms: 1.01x faster                                                      |
| pickle_dict          | 34.8 us                                                    | 34.6 us: 1.01x faster                                                      |
| unpickle             | 15.1 us                                                    | 15.1 us: 1.00x faster                                                      |
| pickle_pure_python   | 305 us                                                     | 306 us: 1.00x slower                                                       |
| unpickle_pure_python | 218 us                                                     | 223 us: 1.02x slower                                                       |
| Geometric mean       | (ref)                                                      | 1.03x faster                                                               |

Benchmark hidden because not significant (2): pickle_list, pickle

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240425-linux-x86_64-brandtbucher-justin_ghccc_cache-3.13.0a6+-280cb86 |
|------------------------|:----------------------------------------------------------:|:--------------------------------------------------------------------------:|
| python_startup         | 10.8 ms                                                    | 11.1 ms: 1.04x slower                                                      |
| python_startup_no_site | 7.11 ms                                                    | 7.71 ms: 1.08x slower                                                      |
| Geometric mean         | (ref)                                                      | 1.06x slower                                                               |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240425-linux-x86_64-brandtbucher-justin_ghccc_cache-3.13.0a6+-280cb86 |
|-----------------|:----------------------------------------------------------:|:--------------------------------------------------------------------------:|
| mako            | 11.2 ms                                                    | 10.0 ms: 1.12x faster                                                      |
| genshi_text     | 23.7 ms                                                    | 24.3 ms: 1.03x slower                                                      |
| django_template | 34.8 ms                                                    | 35.9 ms: 1.03x slower                                                      |
| genshi_xml      | 51.6 ms                                                    | 54.2 ms: 1.05x slower                                                      |
| Geometric mean  | (ref)                                                      | 1.00x faster                                                               |

All benchmarks:
===============

| Benchmark                  | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240425-linux-x86_64-brandtbucher-justin_ghccc_cache-3.13.0a6+-280cb86 |
|----------------------------|:----------------------------------------------------------:|:--------------------------------------------------------------------------:|
| typing_runtime_protocols   | 165 us                                                     | 116 us: 1.42x faster                                                       |
| scimark_fft                | 392 ms                                                     | 308 ms: 1.28x faster                                                       |
| richards                   | 50.9 ms                                                    | 41.9 ms: 1.21x faster                                                      |
| scimark_sparse_mat_mult    | 5.27 ms                                                    | 4.38 ms: 1.20x faster                                                      |
| richards_super             | 57.4 ms                                                    | 48.0 ms: 1.19x faster                                                      |
| nbody                      | 88.3 ms                                                    | 75.3 ms: 1.17x faster                                                      |
| spectral_norm              | 116 ms                                                     | 99.7 ms: 1.17x faster                                                      |
| fannkuch                   | 402 ms                                                     | 345 ms: 1.16x faster                                                       |
| crypto_pyaes               | 77.5 ms                                                    | 67.7 ms: 1.14x faster                                                      |
| mako                       | 11.2 ms                                                    | 10.0 ms: 1.12x faster                                                      |
| pyflate                    | 484 ms                                                     | 432 ms: 1.12x faster                                                       |
| scimark_monte_carlo        | 69.2 ms                                                    | 61.9 ms: 1.12x faster                                                      |
| tomli_loads                | 2.12 sec                                                   | 1.90 sec: 1.12x faster                                                     |
| xml_etree_parse            | 162 ms                                                     | 148 ms: 1.09x faster                                                       |
| float                      | 78.9 ms                                                    | 72.6 ms: 1.09x faster                                                      |
| async_tree_none            | 378 ms                                                     | 356 ms: 1.06x faster                                                       |
| sqlite_synth               | 2.99 us                                                    | 2.82 us: 1.06x faster                                                      |
| xml_etree_iterparse        | 107 ms                                                     | 102 ms: 1.05x faster                                                       |
| pprint_pformat             | 1.56 sec                                                   | 1.48 sec: 1.05x faster                                                     |
| pprint_safe_repr           | 758 ms                                                     | 724 ms: 1.05x faster                                                       |
| json_loads                 | 28.9 us                                                    | 27.6 us: 1.05x faster                                                      |
| deepcopy_reduce            | 3.35 us                                                    | 3.21 us: 1.04x faster                                                      |
| chameleon                  | 7.22 ms                                                    | 6.94 ms: 1.04x faster                                                      |
| unpickle_list              | 5.34 us                                                    | 5.14 us: 1.04x faster                                                      |
| mdp                        | 2.79 sec                                                   | 2.69 sec: 1.04x faster                                                     |
| chaos                      | 61.3 ms                                                    | 59.3 ms: 1.03x faster                                                      |
| create_gc_cycles           | 1.82 ms                                                    | 1.76 ms: 1.03x faster                                                      |
| json                       | 5.31 ms                                                    | 5.15 ms: 1.03x faster                                                      |
| logging_silent             | 105 ns                                                     | 102 ns: 1.03x faster                                                       |
| xml_etree_process          | 61.2 ms                                                    | 59.7 ms: 1.02x faster                                                      |
| coroutines                 | 23.2 ms                                                    | 22.8 ms: 1.01x faster                                                      |
| deepcopy_memo              | 39.7 us                                                    | 39.2 us: 1.01x faster                                                      |
| deepcopy                   | 367 us                                                     | 363 us: 1.01x faster                                                       |
| json_dumps                 | 10.7 ms                                                    | 10.6 ms: 1.01x faster                                                      |
| sqlglot_parse              | 1.32 ms                                                    | 1.31 ms: 1.01x faster                                                      |
| xml_etree_generate         | 87.4 ms                                                    | 86.7 ms: 1.01x faster                                                      |
| thrift                     | 823 us                                                     | 817 us: 1.01x faster                                                       |
| pickle_dict                | 34.8 us                                                    | 34.6 us: 1.01x faster                                                      |
| unpickle                   | 15.1 us                                                    | 15.1 us: 1.00x faster                                                      |
| meteor_contest             | 110 ms                                                     | 109 ms: 1.00x faster                                                       |
| pickle_pure_python         | 305 us                                                     | 306 us: 1.00x slower                                                       |
| 2to3                       | 274 ms                                                     | 275 ms: 1.00x slower                                                       |
| tornado_http               | 94.6 ms                                                    | 95.3 ms: 1.01x slower                                                      |
| bench_mp_pool              | 23.9 ms                                                    | 24.0 ms: 1.01x slower                                                      |
| generators                 | 29.6 ms                                                    | 29.9 ms: 1.01x slower                                                      |
| pidigits                   | 191 ms                                                     | 193 ms: 1.01x slower                                                       |
| asyncio_tcp_ssl            | 1.84 sec                                                   | 1.86 sec: 1.01x slower                                                     |
| gunicorn                   | 1.28 ms                                                    | 1.29 ms: 1.01x slower                                                      |
| logging_simple             | 5.74 us                                                    | 5.82 us: 1.01x slower                                                      |
| regex_v8                   | 25.1 ms                                                    | 25.5 ms: 1.01x slower                                                      |
| html5lib                   | 67.2 ms                                                    | 68.2 ms: 1.01x slower                                                      |
| go                         | 145 ms                                                     | 147 ms: 1.01x slower                                                       |
| djangocms                  | 31.5 us                                                    | 32.0 us: 1.01x slower                                                      |
| asyncio_tcp                | 508 ms                                                     | 516 ms: 1.02x slower                                                       |
| hexiom                     | 6.30 ms                                                    | 6.40 ms: 1.02x slower                                                      |
| raytrace                   | 267 ms                                                     | 271 ms: 1.02x slower                                                       |
| telco                      | 8.41 ms                                                    | 8.57 ms: 1.02x slower                                                      |
| regex_compile              | 137 ms                                                     | 140 ms: 1.02x slower                                                       |
| sqlglot_normalize          | 110 ms                                                     | 113 ms: 1.02x slower                                                       |
| gc_traversal               | 3.98 ms                                                    | 4.06 ms: 1.02x slower                                                      |
| sqlglot_optimize           | 55.5 ms                                                    | 56.7 ms: 1.02x slower                                                      |
| unpickle_pure_python       | 218 us                                                     | 223 us: 1.02x slower                                                       |
| regex_effbot               | 3.67 ms                                                    | 3.76 ms: 1.02x slower                                                      |
| dulwich_log                | 67.2 ms                                                    | 68.8 ms: 1.03x slower                                                      |
| aiohttp                    | 1.18 ms                                                    | 1.21 ms: 1.03x slower                                                      |
| genshi_text                | 23.7 ms                                                    | 24.3 ms: 1.03x slower                                                      |
| comprehensions             | 16.6 us                                                    | 17.1 us: 1.03x slower                                                      |
| scimark_lu                 | 122 ms                                                     | 125 ms: 1.03x slower                                                       |
| async_tree_cpu_io_mixed_tg | 587 ms                                                     | 605 ms: 1.03x slower                                                       |
| bench_thread_pool          | 834 us                                                     | 860 us: 1.03x slower                                                       |
| django_template            | 34.8 ms                                                    | 35.9 ms: 1.03x slower                                                      |
| docutils                   | 2.83 sec                                                   | 2.92 sec: 1.03x slower                                                     |
| sympy_str                  | 282 ms                                                     | 291 ms: 1.03x slower                                                       |
| python_startup             | 10.8 ms                                                    | 11.1 ms: 1.04x slower                                                      |
| regex_dna                  | 221 ms                                                     | 230 ms: 1.04x slower                                                       |
| coverage                   | 93.1 ms                                                    | 97.2 ms: 1.04x slower                                                      |
| pathlib                    | 17.3 ms                                                    | 18.1 ms: 1.05x slower                                                      |
| sympy_expand               | 473 ms                                                     | 494 ms: 1.05x slower                                                       |
| genshi_xml                 | 51.6 ms                                                    | 54.2 ms: 1.05x slower                                                      |
| mypy2                      | 742 ms                                                     | 779 ms: 1.05x slower                                                       |
| async_generators           | 442 ms                                                     | 466 ms: 1.05x slower                                                       |
| nqueens                    | 81.4 ms                                                    | 86.0 ms: 1.06x slower                                                      |
| sympy_sum                  | 156 ms                                                     | 166 ms: 1.06x slower                                                       |
| sympy_integrate            | 20.5 ms                                                    | 21.8 ms: 1.06x slower                                                      |
| python_startup_no_site     | 7.11 ms                                                    | 7.71 ms: 1.08x slower                                                      |
| deltablue                  | 3.25 ms                                                    | 3.63 ms: 1.12x slower                                                      |
| Geometric mean             | (ref)                                                      | 1.02x faster                                                               |

Benchmark hidden because not significant (15): async_tree_memoization_tg, asyncio_websockets, async_tree_memoization, sqlglot_transpile, pickle_list, async_tree_io, scimark_sor, pickle, async_tree_none_tg, async_tree_cpu_io_mixed, pycparser, logging_format, dask, async_tree_io_tg, pylint
Ignored benchmarks (2) of results/bm-20240605-3.13.0b2-3a83b17/bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17.json: bpe_tokeniser, flaskblogging

# HPT report

- Reliability score: 82.90% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.09x