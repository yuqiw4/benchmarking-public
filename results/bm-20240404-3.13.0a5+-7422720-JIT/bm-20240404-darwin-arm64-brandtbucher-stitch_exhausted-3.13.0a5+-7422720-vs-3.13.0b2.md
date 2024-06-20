# Results vs. 3.13.0b2

- fork: brandtbucher
- ref: stitch_exhausted
- machine: darwin-arm64
- commit hash: 7422720
- commit date: 2024-04-04
- overall geometric mean: 1.04x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.02x slower
- Memory change: 1.17x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240605-darwin-arm64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240404-darwin-arm64-brandtbucher-stitch_exhausted-3.13.0a5+-7422720 |
|----------------|:----------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 161 ms                                                     | 173 ms: 1.08x slower                                                     |
| chameleon      | 4.27 ms                                                    | 4.46 ms: 1.05x slower                                                    |
| docutils       | 1.44 sec                                                   | 1.58 sec: 1.10x slower                                                   |
| tornado_http   | 66.7 ms                                                    | 79.8 ms: 1.20x slower                                                    |
| Geometric mean | (ref)                                                      | 1.08x slower                                                             |

Benchmark hidden because not significant (1): html5lib

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240605-darwin-arm64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240404-darwin-arm64-brandtbucher-stitch_exhausted-3.13.0a5+-7422720 |
|----------------------------------|:----------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_none                  | 209 ms                                                     | 204 ms: 1.03x faster                                                     |
| async_tree_eager_cpu_io_mixed_tg | 331 ms                                                     | 334 ms: 1.01x slower                                                     |
| async_tree_eager_cpu_io_mixed    | 358 ms                                                     | 366 ms: 1.02x slower                                                     |
| async_tree_cpu_io_mixed_tg       | 451 ms                                                     | 467 ms: 1.04x slower                                                     |
| async_tree_eager_memoization_tg  | 126 ms                                                     | 131 ms: 1.04x slower                                                     |
| async_tree_eager_tg              | 41.4 ms                                                    | 43.3 ms: 1.05x slower                                                    |
| async_tree_memoization_tg        | 240 ms                                                     | 261 ms: 1.09x slower                                                     |
| async_tree_eager                 | 60.3 ms                                                    | 66.3 ms: 1.10x slower                                                    |
| Geometric mean                   | (ref)                                                      | 1.02x slower                                                             |

Benchmark hidden because not significant (8): async_tree_eager_io_tg, async_tree_cpu_io_mixed, async_tree_io_tg, async_tree_none_tg, async_tree_io, async_tree_memoization, async_tree_eager_io, async_tree_eager_memoization

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240605-darwin-arm64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240404-darwin-arm64-brandtbucher-stitch_exhausted-3.13.0a5+-7422720 |
|----------------|:----------------------------------------------------------:|:------------------------------------------------------------------------:|
| float          | 48.6 ms                                                    | 49.5 ms: 1.02x slower                                                    |
| nbody          | 59.6 ms                                                    | 70.3 ms: 1.18x slower                                                    |
| Geometric mean | (ref)                                                      | 1.06x slower                                                             |

Benchmark hidden because not significant (1): pidigits

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240605-darwin-arm64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240404-darwin-arm64-brandtbucher-stitch_exhausted-3.13.0a5+-7422720 |
|----------------|:----------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_dna      | 149 ms                                                     | 145 ms: 1.03x faster                                                     |
| regex_effbot   | 2.58 ms                                                    | 2.56 ms: 1.01x faster                                                    |
| regex_v8       | 17.3 ms                                                    | 17.2 ms: 1.00x faster                                                    |
| regex_compile  | 68.5 ms                                                    | 86.1 ms: 1.26x slower                                                    |
| Geometric mean | (ref)                                                      | 1.05x slower                                                             |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240605-darwin-arm64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240404-darwin-arm64-brandtbucher-stitch_exhausted-3.13.0a5+-7422720 |
|----------------------|:----------------------------------------------------------:|:------------------------------------------------------------------------:|
| tomli_loads          | 1.47 sec                                                   | 1.29 sec: 1.13x faster                                                   |
| xml_etree_process    | 37.1 ms                                                    | 36.5 ms: 1.02x faster                                                    |
| pickle_dict          | 18.3 us                                                    | 18.1 us: 1.01x faster                                                    |
| unpickle_pure_python | 141 us                                                     | 140 us: 1.01x faster                                                     |
| xml_etree_iterparse  | 71.5 ms                                                    | 72.2 ms: 1.01x slower                                                    |
| json_loads           | 16.8 us                                                    | 17.1 us: 1.01x slower                                                    |
| pickle_list          | 2.96 us                                                    | 3.00 us: 1.01x slower                                                    |
| unpickle             | 9.12 us                                                    | 9.27 us: 1.02x slower                                                    |
| json_dumps           | 6.23 ms                                                    | 6.37 ms: 1.02x slower                                                    |
| pickle_pure_python   | 179 us                                                     | 183 us: 1.03x slower                                                     |
| xml_etree_generate   | 52.7 ms                                                    | 54.3 ms: 1.03x slower                                                    |
| unpickle_list        | 2.88 us                                                    | 3.04 us: 1.06x slower                                                    |
| Geometric mean       | (ref)                                                      | 1.00x slower                                                             |

Benchmark hidden because not significant (2): pickle, xml_etree_parse

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240605-darwin-arm64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240404-darwin-arm64-brandtbucher-stitch_exhausted-3.13.0a5+-7422720 |
|------------------------|:----------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup         | 15.2 ms                                                    | 13.5 ms: 1.13x faster                                                    |
| python_startup_no_site | 12.3 ms                                                    | 11.7 ms: 1.05x faster                                                    |
| Geometric mean         | (ref)                                                      | 1.09x faster                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark      | bm-20240605-darwin-arm64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240404-darwin-arm64-brandtbucher-stitch_exhausted-3.13.0a5+-7422720 |
|----------------|:----------------------------------------------------------:|:------------------------------------------------------------------------:|
| mako           | 6.99 ms                                                    | 6.92 ms: 1.01x faster                                                    |
| genshi_text    | 13.9 ms                                                    | 14.7 ms: 1.06x slower                                                    |
| genshi_xml     | 29.9 ms                                                    | 33.2 ms: 1.11x slower                                                    |
| Geometric mean | (ref)                                                      | 1.05x slower                                                             |

All benchmarks:
===============

| Benchmark                        | bm-20240605-darwin-arm64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240404-darwin-arm64-brandtbucher-stitch_exhausted-3.13.0a5+-7422720 |
|----------------------------------|:----------------------------------------------------------:|:------------------------------------------------------------------------:|
| typing_runtime_protocols         | 87.6 us                                                    | 70.3 us: 1.25x faster                                                    |
| tomli_loads                      | 1.47 sec                                                   | 1.29 sec: 1.13x faster                                                   |
| python_startup                   | 15.2 ms                                                    | 13.5 ms: 1.13x faster                                                    |
| richards                         | 31.8 ms                                                    | 29.1 ms: 1.10x faster                                                    |
| pylint                           | 170 ms                                                     | 157 ms: 1.08x faster                                                     |
| richards_super                   | 35.2 ms                                                    | 32.7 ms: 1.08x faster                                                    |
| crypto_pyaes                     | 49.5 ms                                                    | 46.9 ms: 1.06x faster                                                    |
| python_startup_no_site           | 12.3 ms                                                    | 11.7 ms: 1.05x faster                                                    |
| async_tree_none                  | 209 ms                                                     | 204 ms: 1.03x faster                                                     |
| regex_dna                        | 149 ms                                                     | 145 ms: 1.03x faster                                                     |
| xml_etree_process                | 37.1 ms                                                    | 36.5 ms: 1.02x faster                                                    |
| bench_mp_pool                    | 47.2 ms                                                    | 46.4 ms: 1.02x faster                                                    |
| pickle_dict                      | 18.3 us                                                    | 18.1 us: 1.01x faster                                                    |
| mako                             | 6.99 ms                                                    | 6.92 ms: 1.01x faster                                                    |
| regex_effbot                     | 2.58 ms                                                    | 2.56 ms: 1.01x faster                                                    |
| telco                            | 4.60 ms                                                    | 4.57 ms: 1.01x faster                                                    |
| pyflate                          | 321 ms                                                     | 319 ms: 1.01x faster                                                     |
| unpickle_pure_python             | 141 us                                                     | 140 us: 1.01x faster                                                     |
| create_gc_cycles                 | 897 us                                                     | 893 us: 1.00x faster                                                     |
| regex_v8                         | 17.3 ms                                                    | 17.2 ms: 1.00x faster                                                    |
| asyncio_websockets               | 409 ms                                                     | 408 ms: 1.00x faster                                                     |
| xml_etree_iterparse              | 71.5 ms                                                    | 72.2 ms: 1.01x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 331 ms                                                     | 334 ms: 1.01x slower                                                     |
| json_loads                       | 16.8 us                                                    | 17.1 us: 1.01x slower                                                    |
| pickle_list                      | 2.96 us                                                    | 3.00 us: 1.01x slower                                                    |
| unpickle                         | 9.12 us                                                    | 9.27 us: 1.02x slower                                                    |
| asyncio_tcp_ssl                  | 1.29 sec                                                   | 1.31 sec: 1.02x slower                                                   |
| float                            | 48.6 ms                                                    | 49.5 ms: 1.02x slower                                                    |
| sqlite_synth                     | 1.55 us                                                    | 1.58 us: 1.02x slower                                                    |
| async_tree_eager_cpu_io_mixed    | 358 ms                                                     | 366 ms: 1.02x slower                                                     |
| deepcopy_reduce                  | 1.82 us                                                    | 1.86 us: 1.02x slower                                                    |
| json_dumps                       | 6.23 ms                                                    | 6.37 ms: 1.02x slower                                                    |
| pickle_pure_python               | 179 us                                                     | 183 us: 1.03x slower                                                     |
| thrift                           | 435 us                                                     | 448 us: 1.03x slower                                                     |
| xml_etree_generate               | 52.7 ms                                                    | 54.3 ms: 1.03x slower                                                    |
| mdp                              | 1.53 sec                                                   | 1.58 sec: 1.03x slower                                                   |
| deepcopy                         | 204 us                                                     | 211 us: 1.03x slower                                                     |
| coverage                         | 45.0 ms                                                    | 46.5 ms: 1.03x slower                                                    |
| pycparser                        | 632 ms                                                     | 655 ms: 1.04x slower                                                     |
| async_tree_cpu_io_mixed_tg       | 451 ms                                                     | 467 ms: 1.04x slower                                                     |
| go                               | 101 ms                                                     | 105 ms: 1.04x slower                                                     |
| scimark_monte_carlo              | 42.5 ms                                                    | 44.3 ms: 1.04x slower                                                    |
| logging_simple                   | 3.04 us                                                    | 3.17 us: 1.04x slower                                                    |
| async_tree_eager_memoization_tg  | 126 ms                                                     | 131 ms: 1.04x slower                                                     |
| chameleon                        | 4.27 ms                                                    | 4.46 ms: 1.05x slower                                                    |
| logging_format                   | 3.31 us                                                    | 3.46 us: 1.05x slower                                                    |
| async_tree_eager_tg              | 41.4 ms                                                    | 43.3 ms: 1.05x slower                                                    |
| dulwich_log                      | 27.6 ms                                                    | 29.0 ms: 1.05x slower                                                    |
| fannkuch                         | 248 ms                                                     | 261 ms: 1.05x slower                                                     |
| sqlglot_parse                    | 732 us                                                     | 772 us: 1.06x slower                                                     |
| unpickle_list                    | 2.88 us                                                    | 3.04 us: 1.06x slower                                                    |
| genshi_text                      | 13.9 ms                                                    | 14.7 ms: 1.06x slower                                                    |
| meteor_contest                   | 70.3 ms                                                    | 74.3 ms: 1.06x slower                                                    |
| logging_silent                   | 60.1 ns                                                    | 63.8 ns: 1.06x slower                                                    |
| sqlglot_transpile                | 891 us                                                     | 948 us: 1.06x slower                                                     |
| sympy_expand                     | 226 ms                                                     | 241 ms: 1.07x slower                                                     |
| deepcopy_memo                    | 22.6 us                                                    | 24.2 us: 1.07x slower                                                    |
| async_generators                 | 281 ms                                                     | 300 ms: 1.07x slower                                                     |
| sqlglot_normalize                | 166 ms                                                     | 178 ms: 1.07x slower                                                     |
| coroutines                       | 15.8 ms                                                    | 17.0 ms: 1.07x slower                                                    |
| 2to3                             | 161 ms                                                     | 173 ms: 1.08x slower                                                     |
| pathlib                          | 23.3 ms                                                    | 25.3 ms: 1.08x slower                                                    |
| async_tree_memoization_tg        | 240 ms                                                     | 261 ms: 1.09x slower                                                     |
| pprint_safe_repr                 | 465 ms                                                     | 507 ms: 1.09x slower                                                     |
| sympy_str                        | 131 ms                                                     | 144 ms: 1.09x slower                                                     |
| pprint_pformat                   | 947 ms                                                     | 1.04 sec: 1.10x slower                                                   |
| docutils                         | 1.44 sec                                                   | 1.58 sec: 1.10x slower                                                   |
| async_tree_eager                 | 60.3 ms                                                    | 66.3 ms: 1.10x slower                                                    |
| sqlglot_optimize                 | 30.9 ms                                                    | 34.2 ms: 1.11x slower                                                    |
| bench_thread_pool                | 447 us                                                     | 495 us: 1.11x slower                                                     |
| spectral_norm                    | 66.4 ms                                                    | 73.5 ms: 1.11x slower                                                    |
| genshi_xml                       | 29.9 ms                                                    | 33.2 ms: 1.11x slower                                                    |
| scimark_fft                      | 181 ms                                                     | 201 ms: 1.11x slower                                                     |
| scimark_sor                      | 94.9 ms                                                    | 106 ms: 1.11x slower                                                     |
| raytrace                         | 147 ms                                                     | 165 ms: 1.12x slower                                                     |
| sympy_sum                        | 69.2 ms                                                    | 77.7 ms: 1.12x slower                                                    |
| mypy2                            | 379 ms                                                     | 427 ms: 1.12x slower                                                     |
| scimark_sparse_mat_mult          | 2.77 ms                                                    | 3.13 ms: 1.13x slower                                                    |
| sympy_integrate                  | 10.3 ms                                                    | 11.8 ms: 1.14x slower                                                    |
| generators                       | 22.9 ms                                                    | 26.1 ms: 1.14x slower                                                    |
| chaos                            | 34.0 ms                                                    | 38.9 ms: 1.14x slower                                                    |
| aiohttp                          | 997 us                                                     | 1.14 ms: 1.14x slower                                                    |
| gunicorn                         | 1.04 ms                                                    | 1.19 ms: 1.15x slower                                                    |
| deltablue                        | 2.14 ms                                                    | 2.48 ms: 1.16x slower                                                    |
| nbody                            | 59.6 ms                                                    | 70.3 ms: 1.18x slower                                                    |
| nqueens                          | 52.2 ms                                                    | 62.0 ms: 1.19x slower                                                    |
| tornado_http                     | 66.7 ms                                                    | 79.8 ms: 1.20x slower                                                    |
| comprehensions                   | 10.2 us                                                    | 12.2 us: 1.20x slower                                                    |
| scimark_lu                       | 66.9 ms                                                    | 81.3 ms: 1.22x slower                                                    |
| regex_compile                    | 68.5 ms                                                    | 86.1 ms: 1.26x slower                                                    |
| hexiom                           | 4.06 ms                                                    | 5.15 ms: 1.27x slower                                                    |
| Geometric mean                   | (ref)                                                      | 1.04x slower                                                             |

Benchmark hidden because not significant (16): async_tree_eager_io_tg, async_tree_cpu_io_mixed, async_tree_io_tg, async_tree_none_tg, gc_traversal, pidigits, pickle, html5lib, json, dask, xml_etree_parse, async_tree_io, async_tree_memoization, async_tree_eager_io, async_tree_eager_memoization, asyncio_tcp
Ignored benchmarks (3) of results/bm-20240605-3.13.0b2-3a83b17/bm-20240605-darwin-arm64-python-v3.13.0b2-3.13.0b2-3a83b17.json: bpe_tokeniser, django_template, flaskblogging

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.03x
- 95% likely to have a slowdown of 1.03x
- 99% likely to have a slowdown of 1.02x

# Memory
- memory change: 1.17x