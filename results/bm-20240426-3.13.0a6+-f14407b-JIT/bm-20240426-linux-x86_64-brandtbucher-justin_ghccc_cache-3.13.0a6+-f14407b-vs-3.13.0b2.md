# Results vs. 3.13.0b2

- fork: brandtbucher
- ref: justin_ghccc_cache
- machine: linux-x86_64
- commit hash: f14407b
- commit date: 2024-04-26
- overall geometric mean: 1.01x faster
- HPT reliability: 89.15%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.09x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240426-linux-x86_64-brandtbucher-justin_ghccc_cache-3.13.0a6+-f14407b |
|----------------|:----------------------------------------------------------:|:--------------------------------------------------------------------------:|
| 2to3           | 274 ms                                                     | 275 ms: 1.00x slower                                                       |
| chameleon      | 7.22 ms                                                    | 7.04 ms: 1.03x faster                                                      |
| docutils       | 2.83 sec                                                   | 2.93 sec: 1.04x slower                                                     |
| html5lib       | 67.2 ms                                                    | 68.1 ms: 1.01x slower                                                      |
| tornado_http   | 94.6 ms                                                    | 95.6 ms: 1.01x slower                                                      |
| Geometric mean | (ref)                                                      | 1.01x slower                                                               |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240426-linux-x86_64-brandtbucher-justin_ghccc_cache-3.13.0a6+-f14407b |
|----------------------------|:----------------------------------------------------------:|:--------------------------------------------------------------------------:|
| async_tree_none            | 378 ms                                                     | 355 ms: 1.07x faster                                                       |
| async_tree_cpu_io_mixed_tg | 587 ms                                                     | 607 ms: 1.03x slower                                                       |
| Geometric mean             | (ref)                                                      | 1.01x faster                                                               |

Benchmark hidden because not significant (6): async_tree_io, async_tree_memoization_tg, async_tree_none_tg, async_tree_memoization, async_tree_cpu_io_mixed, async_tree_io_tg

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240426-linux-x86_64-brandtbucher-justin_ghccc_cache-3.13.0a6+-f14407b |
|----------------|:----------------------------------------------------------:|:--------------------------------------------------------------------------:|
| nbody          | 88.3 ms                                                    | 80.0 ms: 1.10x faster                                                      |
| float          | 78.9 ms                                                    | 73.1 ms: 1.08x faster                                                      |
| pidigits       | 191 ms                                                     | 210 ms: 1.10x slower                                                       |
| Geometric mean | (ref)                                                      | 1.03x faster                                                               |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240426-linux-x86_64-brandtbucher-justin_ghccc_cache-3.13.0a6+-f14407b |
|----------------|:----------------------------------------------------------:|:--------------------------------------------------------------------------:|
| regex_v8       | 25.1 ms                                                    | 24.7 ms: 1.01x faster                                                      |
| regex_dna      | 221 ms                                                     | 225 ms: 1.02x slower                                                       |
| regex_compile  | 137 ms                                                     | 141 ms: 1.03x slower                                                       |
| regex_effbot   | 3.67 ms                                                    | 4.23 ms: 1.15x slower                                                      |
| Geometric mean | (ref)                                                      | 1.04x slower                                                               |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240426-linux-x86_64-brandtbucher-justin_ghccc_cache-3.13.0a6+-f14407b |
|----------------------|:----------------------------------------------------------:|:--------------------------------------------------------------------------:|
| tomli_loads          | 2.12 sec                                                   | 1.93 sec: 1.10x faster                                                     |
| xml_etree_parse      | 162 ms                                                     | 149 ms: 1.09x faster                                                       |
| xml_etree_iterparse  | 107 ms                                                     | 102 ms: 1.05x faster                                                       |
| json_loads           | 28.9 us                                                    | 27.4 us: 1.05x faster                                                      |
| unpickle_list        | 5.34 us                                                    | 5.14 us: 1.04x faster                                                      |
| xml_etree_process    | 61.2 ms                                                    | 60.0 ms: 1.02x faster                                                      |
| xml_etree_generate   | 87.4 ms                                                    | 86.8 ms: 1.01x faster                                                      |
| pickle_list          | 5.11 us                                                    | 5.09 us: 1.00x faster                                                      |
| pickle_pure_python   | 305 us                                                     | 308 us: 1.01x slower                                                       |
| unpickle             | 15.1 us                                                    | 15.5 us: 1.03x slower                                                      |
| unpickle_pure_python | 218 us                                                     | 226 us: 1.04x slower                                                       |
| pickle               | 11.5 us                                                    | 12.0 us: 1.04x slower                                                      |
| Geometric mean       | (ref)                                                      | 1.02x faster                                                               |

Benchmark hidden because not significant (2): json_dumps, pickle_dict

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240426-linux-x86_64-brandtbucher-justin_ghccc_cache-3.13.0a6+-f14407b |
|------------------------|:----------------------------------------------------------:|:--------------------------------------------------------------------------:|
| python_startup         | 10.8 ms                                                    | 11.1 ms: 1.03x slower                                                      |
| python_startup_no_site | 7.11 ms                                                    | 7.66 ms: 1.08x slower                                                      |
| Geometric mean         | (ref)                                                      | 1.05x slower                                                               |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240426-linux-x86_64-brandtbucher-justin_ghccc_cache-3.13.0a6+-f14407b |
|-----------------|:----------------------------------------------------------:|:--------------------------------------------------------------------------:|
| mako            | 11.2 ms                                                    | 10.0 ms: 1.12x faster                                                      |
| genshi_xml      | 51.6 ms                                                    | 54.1 ms: 1.05x slower                                                      |
| django_template | 34.8 ms                                                    | 36.7 ms: 1.05x slower                                                      |
| genshi_text     | 23.7 ms                                                    | 25.0 ms: 1.06x slower                                                      |
| Geometric mean  | (ref)                                                      | 1.01x slower                                                               |

All benchmarks:
===============

| Benchmark                  | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240426-linux-x86_64-brandtbucher-justin_ghccc_cache-3.13.0a6+-f14407b |
|----------------------------|:----------------------------------------------------------:|:--------------------------------------------------------------------------:|
| typing_runtime_protocols   | 165 us                                                     | 117 us: 1.41x faster                                                       |
| scimark_fft                | 392 ms                                                     | 310 ms: 1.27x faster                                                       |
| richards                   | 50.9 ms                                                    | 42.4 ms: 1.20x faster                                                      |
| richards_super             | 57.4 ms                                                    | 48.9 ms: 1.17x faster                                                      |
| spectral_norm              | 116 ms                                                     | 99.2 ms: 1.17x faster                                                      |
| scimark_sparse_mat_mult    | 5.27 ms                                                    | 4.55 ms: 1.16x faster                                                      |
| crypto_pyaes               | 77.5 ms                                                    | 67.6 ms: 1.15x faster                                                      |
| fannkuch                   | 402 ms                                                     | 357 ms: 1.13x faster                                                       |
| mako                       | 11.2 ms                                                    | 10.0 ms: 1.12x faster                                                      |
| pyflate                    | 484 ms                                                     | 434 ms: 1.12x faster                                                       |
| scimark_monte_carlo        | 69.2 ms                                                    | 62.5 ms: 1.11x faster                                                      |
| nbody                      | 88.3 ms                                                    | 80.0 ms: 1.10x faster                                                      |
| tomli_loads                | 2.12 sec                                                   | 1.93 sec: 1.10x faster                                                     |
| xml_etree_parse            | 162 ms                                                     | 149 ms: 1.09x faster                                                       |
| float                      | 78.9 ms                                                    | 73.1 ms: 1.08x faster                                                      |
| async_tree_none            | 378 ms                                                     | 355 ms: 1.07x faster                                                       |
| pprint_pformat             | 1.56 sec                                                   | 1.46 sec: 1.06x faster                                                     |
| sqlite_synth               | 2.99 us                                                    | 2.83 us: 1.06x faster                                                      |
| xml_etree_iterparse        | 107 ms                                                     | 102 ms: 1.05x faster                                                       |
| json_loads                 | 28.9 us                                                    | 27.4 us: 1.05x faster                                                      |
| pprint_safe_repr           | 758 ms                                                     | 722 ms: 1.05x faster                                                       |
| deepcopy_reduce            | 3.35 us                                                    | 3.20 us: 1.05x faster                                                      |
| unpickle_list              | 5.34 us                                                    | 5.14 us: 1.04x faster                                                      |
| create_gc_cycles           | 1.82 ms                                                    | 1.75 ms: 1.04x faster                                                      |
| json                       | 5.31 ms                                                    | 5.13 ms: 1.03x faster                                                      |
| gc_traversal               | 3.98 ms                                                    | 3.86 ms: 1.03x faster                                                      |
| chameleon                  | 7.22 ms                                                    | 7.04 ms: 1.03x faster                                                      |
| xml_etree_process          | 61.2 ms                                                    | 60.0 ms: 1.02x faster                                                      |
| coroutines                 | 23.2 ms                                                    | 22.8 ms: 1.02x faster                                                      |
| deepcopy                   | 367 us                                                     | 362 us: 1.01x faster                                                       |
| regex_v8                   | 25.1 ms                                                    | 24.7 ms: 1.01x faster                                                      |
| logging_silent             | 105 ns                                                     | 104 ns: 1.01x faster                                                       |
| sqlglot_parse              | 1.32 ms                                                    | 1.31 ms: 1.01x faster                                                      |
| xml_etree_generate         | 87.4 ms                                                    | 86.8 ms: 1.01x faster                                                      |
| asyncio_websockets         | 567 ms                                                     | 564 ms: 1.00x faster                                                       |
| pickle_list                | 5.11 us                                                    | 5.09 us: 1.00x faster                                                      |
| 2to3                       | 274 ms                                                     | 275 ms: 1.00x slower                                                       |
| scimark_sor                | 127 ms                                                     | 128 ms: 1.01x slower                                                       |
| logging_format             | 6.47 us                                                    | 6.52 us: 1.01x slower                                                      |
| pickle_pure_python         | 305 us                                                     | 308 us: 1.01x slower                                                       |
| asyncio_tcp                | 508 ms                                                     | 513 ms: 1.01x slower                                                       |
| asyncio_tcp_ssl            | 1.84 sec                                                   | 1.86 sec: 1.01x slower                                                     |
| tornado_http               | 94.6 ms                                                    | 95.6 ms: 1.01x slower                                                      |
| html5lib                   | 67.2 ms                                                    | 68.1 ms: 1.01x slower                                                      |
| thrift                     | 823 us                                                     | 834 us: 1.01x slower                                                       |
| go                         | 145 ms                                                     | 147 ms: 1.02x slower                                                       |
| regex_dna                  | 221 ms                                                     | 225 ms: 1.02x slower                                                       |
| gunicorn                   | 1.28 ms                                                    | 1.30 ms: 1.02x slower                                                      |
| djangocms                  | 31.5 us                                                    | 32.2 us: 1.02x slower                                                      |
| aiohttp                    | 1.18 ms                                                    | 1.21 ms: 1.02x slower                                                      |
| raytrace                   | 267 ms                                                     | 274 ms: 1.03x slower                                                       |
| sqlglot_normalize          | 110 ms                                                     | 113 ms: 1.03x slower                                                       |
| unpickle                   | 15.1 us                                                    | 15.5 us: 1.03x slower                                                      |
| sqlglot_optimize           | 55.5 ms                                                    | 57.1 ms: 1.03x slower                                                      |
| regex_compile              | 137 ms                                                     | 141 ms: 1.03x slower                                                       |
| python_startup             | 10.8 ms                                                    | 11.1 ms: 1.03x slower                                                      |
| logging_simple             | 5.74 us                                                    | 5.92 us: 1.03x slower                                                      |
| pathlib                    | 17.3 ms                                                    | 17.9 ms: 1.03x slower                                                      |
| scimark_lu                 | 122 ms                                                     | 125 ms: 1.03x slower                                                       |
| async_tree_cpu_io_mixed_tg | 587 ms                                                     | 607 ms: 1.03x slower                                                       |
| comprehensions             | 16.6 us                                                    | 17.2 us: 1.03x slower                                                      |
| bench_thread_pool          | 834 us                                                     | 863 us: 1.04x slower                                                       |
| dulwich_log                | 67.2 ms                                                    | 69.7 ms: 1.04x slower                                                      |
| docutils                   | 2.83 sec                                                   | 2.93 sec: 1.04x slower                                                     |
| unpickle_pure_python       | 218 us                                                     | 226 us: 1.04x slower                                                       |
| telco                      | 8.41 ms                                                    | 8.74 ms: 1.04x slower                                                      |
| sympy_str                  | 282 ms                                                     | 294 ms: 1.04x slower                                                       |
| hexiom                     | 6.30 ms                                                    | 6.57 ms: 1.04x slower                                                      |
| pickle                     | 11.5 us                                                    | 12.0 us: 1.04x slower                                                      |
| genshi_xml                 | 51.6 ms                                                    | 54.1 ms: 1.05x slower                                                      |
| sympy_expand               | 473 ms                                                     | 496 ms: 1.05x slower                                                       |
| django_template            | 34.8 ms                                                    | 36.7 ms: 1.05x slower                                                      |
| coverage                   | 93.1 ms                                                    | 98.1 ms: 1.05x slower                                                      |
| genshi_text                | 23.7 ms                                                    | 25.0 ms: 1.06x slower                                                      |
| mypy2                      | 742 ms                                                     | 785 ms: 1.06x slower                                                       |
| async_generators           | 442 ms                                                     | 470 ms: 1.06x slower                                                       |
| sympy_sum                  | 156 ms                                                     | 166 ms: 1.07x slower                                                       |
| sympy_integrate            | 20.5 ms                                                    | 21.9 ms: 1.07x slower                                                      |
| nqueens                    | 81.4 ms                                                    | 87.5 ms: 1.08x slower                                                      |
| python_startup_no_site     | 7.11 ms                                                    | 7.66 ms: 1.08x slower                                                      |
| pidigits                   | 191 ms                                                     | 210 ms: 1.10x slower                                                       |
| deltablue                  | 3.25 ms                                                    | 3.72 ms: 1.14x slower                                                      |
| regex_effbot               | 3.67 ms                                                    | 4.23 ms: 1.15x slower                                                      |
| Geometric mean             | (ref)                                                      | 1.01x faster                                                               |

Benchmark hidden because not significant (18): async_tree_io, async_tree_memoization_tg, chaos, async_tree_none_tg, json_dumps, sqlglot_transpile, meteor_contest, pickle_dict, async_tree_memoization, mdp, deepcopy_memo, pycparser, bench_mp_pool, generators, async_tree_cpu_io_mixed, dask, async_tree_io_tg, pylint
Ignored benchmarks (2) of results/bm-20240605-3.13.0b2-3a83b17/bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17.json: bpe_tokeniser, flaskblogging

# HPT report

- Reliability score: 89.15% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.09x