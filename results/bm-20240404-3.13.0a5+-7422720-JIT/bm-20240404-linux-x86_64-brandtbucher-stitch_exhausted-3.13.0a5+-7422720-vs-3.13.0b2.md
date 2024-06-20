# Results vs. 3.13.0b2

- fork: brandtbucher
- ref: stitch_exhausted
- machine: linux-x86_64
- commit hash: 7422720
- commit date: 2024-04-04
- overall geometric mean: 1.01x slower
- HPT reliability: 99.91%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.06x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240404-linux-x86_64-brandtbucher-stitch_exhausted-3.13.0a5+-7422720 |
|----------------|:----------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 274 ms                                                     | 281 ms: 1.03x slower                                                     |
| chameleon      | 7.22 ms                                                    | 6.90 ms: 1.05x faster                                                    |
| docutils       | 2.83 sec                                                   | 2.97 sec: 1.05x slower                                                   |
| html5lib       | 67.2 ms                                                    | 68.6 ms: 1.02x slower                                                    |
| tornado_http   | 94.6 ms                                                    | 97.2 ms: 1.03x slower                                                    |
| Geometric mean | (ref)                                                      | 1.02x slower                                                             |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240404-linux-x86_64-brandtbucher-stitch_exhausted-3.13.0a5+-7422720 |
|----------------------------|:----------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_none            | 378 ms                                                     | 358 ms: 1.06x faster                                                     |
| async_tree_cpu_io_mixed_tg | 587 ms                                                     | 610 ms: 1.04x slower                                                     |
| Geometric mean             | (ref)                                                      | 1.00x faster                                                             |

Benchmark hidden because not significant (6): async_tree_memoization, async_tree_io, async_tree_memoization_tg, async_tree_io_tg, async_tree_none_tg, async_tree_cpu_io_mixed

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240404-linux-x86_64-brandtbucher-stitch_exhausted-3.13.0a5+-7422720 |
|----------------|:----------------------------------------------------------:|:------------------------------------------------------------------------:|
| float          | 78.9 ms                                                    | 76.5 ms: 1.03x faster                                                    |
| pidigits       | 191 ms                                                     | 189 ms: 1.01x faster                                                     |
| nbody          | 88.3 ms                                                    | 91.3 ms: 1.03x slower                                                    |
| Geometric mean | (ref)                                                      | 1.00x faster                                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240404-linux-x86_64-brandtbucher-stitch_exhausted-3.13.0a5+-7422720 |
|----------------|:----------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_effbot   | 3.67 ms                                                    | 3.70 ms: 1.01x slower                                                    |
| regex_dna      | 221 ms                                                     | 223 ms: 1.01x slower                                                     |
| regex_v8       | 25.1 ms                                                    | 25.5 ms: 1.01x slower                                                    |
| regex_compile  | 137 ms                                                     | 145 ms: 1.06x slower                                                     |
| Geometric mean | (ref)                                                      | 1.02x slower                                                             |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240404-linux-x86_64-brandtbucher-stitch_exhausted-3.13.0a5+-7422720 |
|----------------------|:----------------------------------------------------------:|:------------------------------------------------------------------------:|
| pickle_list          | 5.11 us                                                    | 4.90 us: 1.04x faster                                                    |
| tomli_loads          | 2.12 sec                                                   | 2.06 sec: 1.03x faster                                                   |
| json_loads           | 28.9 us                                                    | 28.1 us: 1.03x faster                                                    |
| json_dumps           | 10.7 ms                                                    | 10.5 ms: 1.03x faster                                                    |
| pickle_dict          | 34.8 us                                                    | 34.2 us: 1.02x faster                                                    |
| xml_etree_process    | 61.2 ms                                                    | 60.2 ms: 1.02x faster                                                    |
| unpickle_list        | 5.34 us                                                    | 5.32 us: 1.00x faster                                                    |
| xml_etree_generate   | 87.4 ms                                                    | 87.8 ms: 1.00x slower                                                    |
| pickle               | 11.5 us                                                    | 11.6 us: 1.01x slower                                                    |
| unpickle             | 15.1 us                                                    | 15.6 us: 1.03x slower                                                    |
| unpickle_pure_python | 218 us                                                     | 242 us: 1.11x slower                                                     |
| Geometric mean       | (ref)                                                      | 1.00x faster                                                             |

Benchmark hidden because not significant (3): pickle_pure_python, xml_etree_iterparse, xml_etree_parse

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240404-linux-x86_64-brandtbucher-stitch_exhausted-3.13.0a5+-7422720 |
|------------------------|:----------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup         | 10.8 ms                                                    | 11.1 ms: 1.03x slower                                                    |
| python_startup_no_site | 7.11 ms                                                    | 9.57 ms: 1.35x slower                                                    |
| Geometric mean         | (ref)                                                      | 1.18x slower                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark      | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240404-linux-x86_64-brandtbucher-stitch_exhausted-3.13.0a5+-7422720 |
|----------------|:----------------------------------------------------------:|:------------------------------------------------------------------------:|
| mako           | 11.2 ms                                                    | 10.6 ms: 1.06x faster                                                    |
| genshi_text    | 23.7 ms                                                    | 24.7 ms: 1.04x slower                                                    |
| genshi_xml     | 51.6 ms                                                    | 55.4 ms: 1.07x slower                                                    |
| Geometric mean | (ref)                                                      | 1.02x slower                                                             |

All benchmarks:
===============

| Benchmark                  | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240404-linux-x86_64-brandtbucher-stitch_exhausted-3.13.0a5+-7422720 |
|----------------------------|:----------------------------------------------------------:|:------------------------------------------------------------------------:|
| typing_runtime_protocols   | 165 us                                                     | 116 us: 1.42x faster                                                     |
| richards                   | 50.9 ms                                                    | 43.3 ms: 1.18x faster                                                    |
| scimark_fft                | 392 ms                                                     | 337 ms: 1.16x faster                                                     |
| richards_super             | 57.4 ms                                                    | 49.7 ms: 1.15x faster                                                    |
| gc_traversal               | 3.98 ms                                                    | 3.61 ms: 1.10x faster                                                    |
| scimark_sparse_mat_mult    | 5.27 ms                                                    | 4.86 ms: 1.08x faster                                                    |
| mako                       | 11.2 ms                                                    | 10.6 ms: 1.06x faster                                                    |
| async_tree_none            | 378 ms                                                     | 358 ms: 1.06x faster                                                     |
| mdp                        | 2.79 sec                                                   | 2.66 sec: 1.05x faster                                                   |
| chameleon                  | 7.22 ms                                                    | 6.90 ms: 1.05x faster                                                    |
| pickle_list                | 5.11 us                                                    | 4.90 us: 1.04x faster                                                    |
| create_gc_cycles           | 1.82 ms                                                    | 1.76 ms: 1.03x faster                                                    |
| logging_silent             | 105 ns                                                     | 101 ns: 1.03x faster                                                     |
| spectral_norm              | 116 ms                                                     | 113 ms: 1.03x faster                                                     |
| float                      | 78.9 ms                                                    | 76.5 ms: 1.03x faster                                                    |
| tomli_loads                | 2.12 sec                                                   | 2.06 sec: 1.03x faster                                                   |
| sqlite_synth               | 2.99 us                                                    | 2.90 us: 1.03x faster                                                    |
| coroutines                 | 23.2 ms                                                    | 22.5 ms: 1.03x faster                                                    |
| json_loads                 | 28.9 us                                                    | 28.1 us: 1.03x faster                                                    |
| json_dumps                 | 10.7 ms                                                    | 10.5 ms: 1.03x faster                                                    |
| deepcopy_reduce            | 3.35 us                                                    | 3.27 us: 1.02x faster                                                    |
| crypto_pyaes               | 77.5 ms                                                    | 76.0 ms: 1.02x faster                                                    |
| pickle_dict                | 34.8 us                                                    | 34.2 us: 1.02x faster                                                    |
| xml_etree_process          | 61.2 ms                                                    | 60.2 ms: 1.02x faster                                                    |
| scimark_monte_carlo        | 69.2 ms                                                    | 68.2 ms: 1.01x faster                                                    |
| deepcopy_memo              | 39.7 us                                                    | 39.2 us: 1.01x faster                                                    |
| pyflate                    | 484 ms                                                     | 478 ms: 1.01x faster                                                     |
| pidigits                   | 191 ms                                                     | 189 ms: 1.01x faster                                                     |
| thrift                     | 823 us                                                     | 816 us: 1.01x faster                                                     |
| json                       | 5.31 ms                                                    | 5.26 ms: 1.01x faster                                                    |
| unpickle_list              | 5.34 us                                                    | 5.32 us: 1.00x faster                                                    |
| xml_etree_generate         | 87.4 ms                                                    | 87.8 ms: 1.00x slower                                                    |
| sqlglot_parse              | 1.32 ms                                                    | 1.33 ms: 1.01x slower                                                    |
| deepcopy                   | 367 us                                                     | 370 us: 1.01x slower                                                     |
| regex_effbot               | 3.67 ms                                                    | 3.70 ms: 1.01x slower                                                    |
| regex_dna                  | 221 ms                                                     | 223 ms: 1.01x slower                                                     |
| logging_format             | 6.47 us                                                    | 6.54 us: 1.01x slower                                                    |
| asyncio_tcp_ssl            | 1.84 sec                                                   | 1.86 sec: 1.01x slower                                                   |
| sqlglot_transpile          | 1.63 ms                                                    | 1.65 ms: 1.01x slower                                                    |
| regex_v8                   | 25.1 ms                                                    | 25.5 ms: 1.01x slower                                                    |
| pickle                     | 11.5 us                                                    | 11.6 us: 1.01x slower                                                    |
| generators                 | 29.6 ms                                                    | 30.1 ms: 1.02x slower                                                    |
| telco                      | 8.41 ms                                                    | 8.58 ms: 1.02x slower                                                    |
| html5lib                   | 67.2 ms                                                    | 68.6 ms: 1.02x slower                                                    |
| meteor_contest             | 110 ms                                                     | 113 ms: 1.02x slower                                                     |
| 2to3                       | 274 ms                                                     | 281 ms: 1.03x slower                                                     |
| tornado_http               | 94.6 ms                                                    | 97.2 ms: 1.03x slower                                                    |
| dask                       | 369 ms                                                     | 379 ms: 1.03x slower                                                     |
| gunicorn                   | 1.28 ms                                                    | 1.31 ms: 1.03x slower                                                    |
| aiohttp                    | 1.18 ms                                                    | 1.21 ms: 1.03x slower                                                    |
| chaos                      | 61.3 ms                                                    | 63.1 ms: 1.03x slower                                                    |
| python_startup             | 10.8 ms                                                    | 11.1 ms: 1.03x slower                                                    |
| logging_simple             | 5.74 us                                                    | 5.93 us: 1.03x slower                                                    |
| go                         | 145 ms                                                     | 149 ms: 1.03x slower                                                     |
| raytrace                   | 267 ms                                                     | 276 ms: 1.03x slower                                                     |
| nbody                      | 88.3 ms                                                    | 91.3 ms: 1.03x slower                                                    |
| unpickle                   | 15.1 us                                                    | 15.6 us: 1.03x slower                                                    |
| bench_thread_pool          | 834 us                                                     | 864 us: 1.04x slower                                                     |
| asyncio_tcp                | 508 ms                                                     | 527 ms: 1.04x slower                                                     |
| async_tree_cpu_io_mixed_tg | 587 ms                                                     | 610 ms: 1.04x slower                                                     |
| genshi_text                | 23.7 ms                                                    | 24.7 ms: 1.04x slower                                                    |
| sqlglot_normalize          | 110 ms                                                     | 115 ms: 1.04x slower                                                     |
| sqlglot_optimize           | 55.5 ms                                                    | 58.1 ms: 1.05x slower                                                    |
| dulwich_log                | 67.2 ms                                                    | 70.4 ms: 1.05x slower                                                    |
| async_generators           | 442 ms                                                     | 464 ms: 1.05x slower                                                     |
| docutils                   | 2.83 sec                                                   | 2.97 sec: 1.05x slower                                                   |
| sympy_str                  | 282 ms                                                     | 300 ms: 1.06x slower                                                     |
| regex_compile              | 137 ms                                                     | 145 ms: 1.06x slower                                                     |
| pycparser                  | 1.16 sec                                                   | 1.23 sec: 1.06x slower                                                   |
| coverage                   | 93.1 ms                                                    | 99.0 ms: 1.06x slower                                                    |
| sympy_expand               | 473 ms                                                     | 504 ms: 1.07x slower                                                     |
| scimark_lu                 | 122 ms                                                     | 130 ms: 1.07x slower                                                     |
| genshi_xml                 | 51.6 ms                                                    | 55.4 ms: 1.07x slower                                                    |
| scimark_sor                | 127 ms                                                     | 138 ms: 1.08x slower                                                     |
| mypy2                      | 742 ms                                                     | 812 ms: 1.09x slower                                                     |
| sympy_sum                  | 156 ms                                                     | 171 ms: 1.10x slower                                                     |
| sympy_integrate            | 20.5 ms                                                    | 22.6 ms: 1.10x slower                                                    |
| unpickle_pure_python       | 218 us                                                     | 242 us: 1.11x slower                                                     |
| comprehensions             | 16.6 us                                                    | 18.6 us: 1.12x slower                                                    |
| pathlib                    | 17.3 ms                                                    | 19.5 ms: 1.13x slower                                                    |
| hexiom                     | 6.30 ms                                                    | 7.17 ms: 1.14x slower                                                    |
| nqueens                    | 81.4 ms                                                    | 93.1 ms: 1.14x slower                                                    |
| deltablue                  | 3.25 ms                                                    | 3.82 ms: 1.18x slower                                                    |
| python_startup_no_site     | 7.11 ms                                                    | 9.57 ms: 1.35x slower                                                    |
| Geometric mean             | (ref)                                                      | 1.01x slower                                                             |

Benchmark hidden because not significant (15): pylint, async_tree_memoization, pprint_safe_repr, pprint_pformat, pickle_pure_python, xml_etree_iterparse, asyncio_websockets, async_tree_io, async_tree_memoization_tg, fannkuch, xml_etree_parse, async_tree_io_tg, bench_mp_pool, async_tree_none_tg, async_tree_cpu_io_mixed
Ignored benchmarks (4) of results/bm-20240605-3.13.0b2-3a83b17/bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17.json: bpe_tokeniser, django_template, djangocms, flaskblogging

# HPT report

- Reliability score: 99.91% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.06x