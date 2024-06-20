# Results vs. 3.13.0b2

- fork: brandtbucher
- ref: justin_ghccc_perf
- machine: linux-x86_64
- commit hash: f7a4afd
- commit date: 2024-04-23
- overall geometric mean: 1.01x faster
- HPT reliability: 96.77%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.06x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240423-linux-x86_64-brandtbucher-justin_ghccc_perf-3.13.0a6+-f7a4afd |
|----------------|:----------------------------------------------------------:|:-------------------------------------------------------------------------:|
| 2to3           | 274 ms                                                     | 275 ms: 1.00x slower                                                      |
| chameleon      | 7.22 ms                                                    | 7.00 ms: 1.03x faster                                                     |
| docutils       | 2.83 sec                                                   | 2.91 sec: 1.03x slower                                                    |
| html5lib       | 67.2 ms                                                    | 68.2 ms: 1.01x slower                                                     |
| tornado_http   | 94.6 ms                                                    | 95.7 ms: 1.01x slower                                                     |
| Geometric mean | (ref)                                                      | 1.01x slower                                                              |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240423-linux-x86_64-brandtbucher-justin_ghccc_perf-3.13.0a6+-f7a4afd |
|----------------------------|:----------------------------------------------------------:|:-------------------------------------------------------------------------:|
| async_tree_none            | 378 ms                                                     | 360 ms: 1.05x faster                                                      |
| async_tree_cpu_io_mixed_tg | 587 ms                                                     | 612 ms: 1.04x slower                                                      |
| Geometric mean             | (ref)                                                      | 1.00x slower                                                              |

Benchmark hidden because not significant (6): async_tree_memoization, async_tree_io, async_tree_memoization_tg, async_tree_none_tg, async_tree_cpu_io_mixed, async_tree_io_tg

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240423-linux-x86_64-brandtbucher-justin_ghccc_perf-3.13.0a6+-f7a4afd |
|----------------|:----------------------------------------------------------:|:-------------------------------------------------------------------------:|
| nbody          | 88.3 ms                                                    | 82.4 ms: 1.07x faster                                                     |
| float          | 78.9 ms                                                    | 74.9 ms: 1.05x faster                                                     |
| pidigits       | 191 ms                                                     | 192 ms: 1.00x slower                                                      |
| Geometric mean | (ref)                                                      | 1.04x faster                                                              |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240423-linux-x86_64-brandtbucher-justin_ghccc_perf-3.13.0a6+-f7a4afd |
|----------------|:----------------------------------------------------------:|:-------------------------------------------------------------------------:|
| regex_v8       | 25.1 ms                                                    | 24.6 ms: 1.02x faster                                                     |
| regex_dna      | 221 ms                                                     | 225 ms: 1.02x slower                                                      |
| regex_compile  | 137 ms                                                     | 140 ms: 1.02x slower                                                      |
| regex_effbot   | 3.67 ms                                                    | 3.80 ms: 1.04x slower                                                     |
| Geometric mean | (ref)                                                      | 1.01x slower                                                              |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240423-linux-x86_64-brandtbucher-justin_ghccc_perf-3.13.0a6+-f7a4afd |
|----------------------|:----------------------------------------------------------:|:-------------------------------------------------------------------------:|
| tomli_loads          | 2.12 sec                                                   | 1.96 sec: 1.08x faster                                                    |
| xml_etree_parse      | 162 ms                                                     | 150 ms: 1.08x faster                                                      |
| xml_etree_iterparse  | 107 ms                                                     | 103 ms: 1.05x faster                                                      |
| unpickle_list        | 5.34 us                                                    | 5.18 us: 1.03x faster                                                     |
| json_loads           | 28.9 us                                                    | 28.3 us: 1.02x faster                                                     |
| xml_etree_process    | 61.2 ms                                                    | 60.0 ms: 1.02x faster                                                     |
| json_dumps           | 10.7 ms                                                    | 10.5 ms: 1.02x faster                                                     |
| pickle_dict          | 34.8 us                                                    | 34.4 us: 1.01x faster                                                     |
| xml_etree_generate   | 87.4 ms                                                    | 86.7 ms: 1.01x faster                                                     |
| unpickle             | 15.1 us                                                    | 15.2 us: 1.00x slower                                                     |
| pickle_pure_python   | 305 us                                                     | 307 us: 1.01x slower                                                      |
| pickle_list          | 5.11 us                                                    | 5.17 us: 1.01x slower                                                     |
| pickle               | 11.5 us                                                    | 11.7 us: 1.02x slower                                                     |
| unpickle_pure_python | 218 us                                                     | 227 us: 1.04x slower                                                      |
| Geometric mean       | (ref)                                                      | 1.02x faster                                                              |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240423-linux-x86_64-brandtbucher-justin_ghccc_perf-3.13.0a6+-f7a4afd |
|------------------------|:----------------------------------------------------------:|:-------------------------------------------------------------------------:|
| python_startup         | 10.8 ms                                                    | 11.0 ms: 1.02x slower                                                     |
| python_startup_no_site | 7.11 ms                                                    | 7.60 ms: 1.07x slower                                                     |
| Geometric mean         | (ref)                                                      | 1.05x slower                                                              |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240423-linux-x86_64-brandtbucher-justin_ghccc_perf-3.13.0a6+-f7a4afd |
|-----------------|:----------------------------------------------------------:|:-------------------------------------------------------------------------:|
| mako            | 11.2 ms                                                    | 10.1 ms: 1.12x faster                                                     |
| genshi_text     | 23.7 ms                                                    | 24.6 ms: 1.04x slower                                                     |
| django_template | 34.8 ms                                                    | 36.7 ms: 1.05x slower                                                     |
| genshi_xml      | 51.6 ms                                                    | 54.5 ms: 1.06x slower                                                     |
| Geometric mean  | (ref)                                                      | 1.01x slower                                                              |

All benchmarks:
===============

| Benchmark                  | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240423-linux-x86_64-brandtbucher-justin_ghccc_perf-3.13.0a6+-f7a4afd |
|----------------------------|:----------------------------------------------------------:|:-------------------------------------------------------------------------:|
| typing_runtime_protocols   | 165 us                                                     | 112 us: 1.47x faster                                                      |
| scimark_fft                | 392 ms                                                     | 315 ms: 1.25x faster                                                      |
| richards                   | 50.9 ms                                                    | 42.3 ms: 1.20x faster                                                     |
| spectral_norm              | 116 ms                                                     | 97.8 ms: 1.19x faster                                                     |
| richards_super             | 57.4 ms                                                    | 48.9 ms: 1.17x faster                                                     |
| scimark_sparse_mat_mult    | 5.27 ms                                                    | 4.62 ms: 1.14x faster                                                     |
| mako                       | 11.2 ms                                                    | 10.1 ms: 1.12x faster                                                     |
| crypto_pyaes               | 77.5 ms                                                    | 69.6 ms: 1.11x faster                                                     |
| fannkuch                   | 402 ms                                                     | 364 ms: 1.11x faster                                                      |
| pyflate                    | 484 ms                                                     | 444 ms: 1.09x faster                                                      |
| tomli_loads                | 2.12 sec                                                   | 1.96 sec: 1.08x faster                                                    |
| xml_etree_parse            | 162 ms                                                     | 150 ms: 1.08x faster                                                      |
| scimark_monte_carlo        | 69.2 ms                                                    | 64.2 ms: 1.08x faster                                                     |
| nbody                      | 88.3 ms                                                    | 82.4 ms: 1.07x faster                                                     |
| float                      | 78.9 ms                                                    | 74.9 ms: 1.05x faster                                                     |
| async_tree_none            | 378 ms                                                     | 360 ms: 1.05x faster                                                      |
| xml_etree_iterparse        | 107 ms                                                     | 103 ms: 1.05x faster                                                      |
| gc_traversal               | 3.98 ms                                                    | 3.80 ms: 1.05x faster                                                     |
| sqlite_synth               | 2.99 us                                                    | 2.86 us: 1.05x faster                                                     |
| coroutines                 | 23.2 ms                                                    | 22.2 ms: 1.04x faster                                                     |
| deepcopy_reduce            | 3.35 us                                                    | 3.23 us: 1.04x faster                                                     |
| logging_silent             | 105 ns                                                     | 101 ns: 1.03x faster                                                      |
| pprint_pformat             | 1.56 sec                                                   | 1.51 sec: 1.03x faster                                                    |
| unpickle_list              | 5.34 us                                                    | 5.18 us: 1.03x faster                                                     |
| chameleon                  | 7.22 ms                                                    | 7.00 ms: 1.03x faster                                                     |
| json                       | 5.31 ms                                                    | 5.15 ms: 1.03x faster                                                     |
| create_gc_cycles           | 1.82 ms                                                    | 1.77 ms: 1.02x faster                                                     |
| deepcopy_memo              | 39.7 us                                                    | 38.8 us: 1.02x faster                                                     |
| pprint_safe_repr           | 758 ms                                                     | 741 ms: 1.02x faster                                                      |
| regex_v8                   | 25.1 ms                                                    | 24.6 ms: 1.02x faster                                                     |
| json_loads                 | 28.9 us                                                    | 28.3 us: 1.02x faster                                                     |
| deepcopy                   | 367 us                                                     | 360 us: 1.02x faster                                                      |
| xml_etree_process          | 61.2 ms                                                    | 60.0 ms: 1.02x faster                                                     |
| json_dumps                 | 10.7 ms                                                    | 10.5 ms: 1.02x faster                                                     |
| pickle_dict                | 34.8 us                                                    | 34.4 us: 1.01x faster                                                     |
| chaos                      | 61.3 ms                                                    | 60.7 ms: 1.01x faster                                                     |
| xml_etree_generate         | 87.4 ms                                                    | 86.7 ms: 1.01x faster                                                     |
| meteor_contest             | 110 ms                                                     | 109 ms: 1.00x faster                                                      |
| pidigits                   | 191 ms                                                     | 192 ms: 1.00x slower                                                      |
| unpickle                   | 15.1 us                                                    | 15.2 us: 1.00x slower                                                     |
| sqlglot_transpile          | 1.63 ms                                                    | 1.64 ms: 1.00x slower                                                     |
| 2to3                       | 274 ms                                                     | 275 ms: 1.00x slower                                                      |
| pickle_pure_python         | 305 us                                                     | 307 us: 1.01x slower                                                      |
| generators                 | 29.6 ms                                                    | 29.8 ms: 1.01x slower                                                     |
| thrift                     | 823 us                                                     | 830 us: 1.01x slower                                                      |
| asyncio_tcp                | 508 ms                                                     | 513 ms: 1.01x slower                                                      |
| asyncio_tcp_ssl            | 1.84 sec                                                   | 1.86 sec: 1.01x slower                                                    |
| tornado_http               | 94.6 ms                                                    | 95.7 ms: 1.01x slower                                                     |
| pickle_list                | 5.11 us                                                    | 5.17 us: 1.01x slower                                                     |
| logging_format             | 6.47 us                                                    | 6.56 us: 1.01x slower                                                     |
| html5lib                   | 67.2 ms                                                    | 68.2 ms: 1.01x slower                                                     |
| regex_dna                  | 221 ms                                                     | 225 ms: 1.02x slower                                                      |
| gunicorn                   | 1.28 ms                                                    | 1.30 ms: 1.02x slower                                                     |
| mdp                        | 2.79 sec                                                   | 2.84 sec: 1.02x slower                                                    |
| raytrace                   | 267 ms                                                     | 272 ms: 1.02x slower                                                      |
| pickle                     | 11.5 us                                                    | 11.7 us: 1.02x slower                                                     |
| bench_thread_pool          | 834 us                                                     | 853 us: 1.02x slower                                                      |
| aiohttp                    | 1.18 ms                                                    | 1.21 ms: 1.02x slower                                                     |
| regex_compile              | 137 ms                                                     | 140 ms: 1.02x slower                                                      |
| python_startup             | 10.8 ms                                                    | 11.0 ms: 1.02x slower                                                     |
| dulwich_log                | 67.2 ms                                                    | 68.9 ms: 1.03x slower                                                     |
| sqlglot_normalize          | 110 ms                                                     | 113 ms: 1.03x slower                                                      |
| pathlib                    | 17.3 ms                                                    | 17.8 ms: 1.03x slower                                                     |
| comprehensions             | 16.6 us                                                    | 17.1 us: 1.03x slower                                                     |
| telco                      | 8.41 ms                                                    | 8.67 ms: 1.03x slower                                                     |
| docutils                   | 2.83 sec                                                   | 2.91 sec: 1.03x slower                                                    |
| sqlglot_optimize           | 55.5 ms                                                    | 57.3 ms: 1.03x slower                                                     |
| logging_simple             | 5.74 us                                                    | 5.94 us: 1.03x slower                                                     |
| regex_effbot               | 3.67 ms                                                    | 3.80 ms: 1.04x slower                                                     |
| sympy_str                  | 282 ms                                                     | 293 ms: 1.04x slower                                                      |
| genshi_text                | 23.7 ms                                                    | 24.6 ms: 1.04x slower                                                     |
| unpickle_pure_python       | 218 us                                                     | 227 us: 1.04x slower                                                      |
| async_tree_cpu_io_mixed_tg | 587 ms                                                     | 612 ms: 1.04x slower                                                      |
| hexiom                     | 6.30 ms                                                    | 6.58 ms: 1.04x slower                                                     |
| sympy_expand               | 473 ms                                                     | 496 ms: 1.05x slower                                                      |
| async_generators           | 442 ms                                                     | 465 ms: 1.05x slower                                                      |
| django_template            | 34.8 ms                                                    | 36.7 ms: 1.05x slower                                                     |
| scimark_lu                 | 122 ms                                                     | 128 ms: 1.05x slower                                                      |
| mypy2                      | 742 ms                                                     | 783 ms: 1.06x slower                                                      |
| genshi_xml                 | 51.6 ms                                                    | 54.5 ms: 1.06x slower                                                     |
| coverage                   | 93.1 ms                                                    | 98.6 ms: 1.06x slower                                                     |
| sympy_integrate            | 20.5 ms                                                    | 21.9 ms: 1.07x slower                                                     |
| go                         | 145 ms                                                     | 154 ms: 1.07x slower                                                      |
| sympy_sum                  | 156 ms                                                     | 166 ms: 1.07x slower                                                      |
| python_startup_no_site     | 7.11 ms                                                    | 7.60 ms: 1.07x slower                                                     |
| nqueens                    | 81.4 ms                                                    | 87.9 ms: 1.08x slower                                                     |
| deltablue                  | 3.25 ms                                                    | 3.68 ms: 1.13x slower                                                     |
| Geometric mean             | (ref)                                                      | 1.01x faster                                                              |

Benchmark hidden because not significant (14): async_tree_memoization, async_tree_io, asyncio_websockets, sqlglot_parse, scimark_sor, bench_mp_pool, pycparser, async_tree_memoization_tg, async_tree_none_tg, async_tree_cpu_io_mixed, dask, async_tree_io_tg, djangocms, pylint
Ignored benchmarks (2) of results/bm-20240605-3.13.0b2-3a83b17/bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17.json: bpe_tokeniser, flaskblogging

# HPT report

- Reliability score: 96.77% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.06x