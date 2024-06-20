# Results vs. 3.13.0b2

- fork: brandtbucher
- ref: justin_trampolines
- machine: darwin-arm64
- commit hash: 6e8e3d5
- commit date: 2024-05-02
- overall geometric mean: 1.03x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.01x slower
- Memory change: 1.18x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240605-darwin-arm64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240502-darwin-arm64-brandtbucher-justin_trampolines-3.13.0a6+-6e8e3d5 |
|----------------|:----------------------------------------------------------:|:--------------------------------------------------------------------------:|
| 2to3           | 161 ms                                                     | 170 ms: 1.06x slower                                                       |
| chameleon      | 4.27 ms                                                    | 4.43 ms: 1.04x slower                                                      |
| docutils       | 1.44 sec                                                   | 1.50 sec: 1.05x slower                                                     |
| html5lib       | 31.2 ms                                                    | 30.9 ms: 1.01x faster                                                      |
| tornado_http   | 66.7 ms                                                    | 72.1 ms: 1.08x slower                                                      |
| Geometric mean | (ref)                                                      | 1.04x slower                                                               |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240605-darwin-arm64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240502-darwin-arm64-brandtbucher-justin_trampolines-3.13.0a6+-6e8e3d5 |
|----------------------------------|:----------------------------------------------------------:|:--------------------------------------------------------------------------:|
| async_tree_none                  | 209 ms                                                     | 200 ms: 1.05x faster                                                       |
| async_tree_eager_cpu_io_mixed_tg | 331 ms                                                     | 334 ms: 1.01x slower                                                       |
| async_tree_eager_cpu_io_mixed    | 358 ms                                                     | 365 ms: 1.02x slower                                                       |
| async_tree_cpu_io_mixed_tg       | 451 ms                                                     | 466 ms: 1.03x slower                                                       |
| async_tree_eager_memoization_tg  | 126 ms                                                     | 130 ms: 1.04x slower                                                       |
| async_tree_eager_tg              | 41.4 ms                                                    | 43.1 ms: 1.04x slower                                                      |
| async_tree_eager                 | 60.3 ms                                                    | 64.8 ms: 1.07x slower                                                      |
| async_tree_memoization_tg        | 240 ms                                                     | 258 ms: 1.08x slower                                                       |
| Geometric mean                   | (ref)                                                      | 1.01x slower                                                               |

Benchmark hidden because not significant (8): async_tree_eager_io_tg, async_tree_cpu_io_mixed, async_tree_io_tg, async_tree_io, async_tree_none_tg, async_tree_eager_io, async_tree_eager_memoization, async_tree_memoization

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240605-darwin-arm64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240502-darwin-arm64-brandtbucher-justin_trampolines-3.13.0a6+-6e8e3d5 |
|----------------|:----------------------------------------------------------:|:--------------------------------------------------------------------------:|
| float          | 48.6 ms                                                    | 49.4 ms: 1.02x slower                                                      |
| nbody          | 59.6 ms                                                    | 67.8 ms: 1.14x slower                                                      |
| Geometric mean | (ref)                                                      | 1.05x slower                                                               |

Benchmark hidden because not significant (1): pidigits

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240605-darwin-arm64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240502-darwin-arm64-brandtbucher-justin_trampolines-3.13.0a6+-6e8e3d5 |
|----------------|:----------------------------------------------------------:|:--------------------------------------------------------------------------:|
| regex_effbot   | 2.58 ms                                                    | 2.57 ms: 1.01x faster                                                      |
| regex_v8       | 17.3 ms                                                    | 17.3 ms: 1.00x slower                                                      |
| regex_compile  | 68.5 ms                                                    | 71.5 ms: 1.04x slower                                                      |
| Geometric mean | (ref)                                                      | 1.01x slower                                                               |

Benchmark hidden because not significant (1): regex_dna

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240605-darwin-arm64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240502-darwin-arm64-brandtbucher-justin_trampolines-3.13.0a6+-6e8e3d5 |
|----------------------|:----------------------------------------------------------:|:--------------------------------------------------------------------------:|
| tomli_loads          | 1.47 sec                                                   | 1.22 sec: 1.20x faster                                                     |
| unpickle_pure_python | 141 us                                                     | 129 us: 1.09x faster                                                       |
| pickle               | 7.48 us                                                    | 7.20 us: 1.04x faster                                                      |
| xml_etree_process    | 37.1 ms                                                    | 35.7 ms: 1.04x faster                                                      |
| xml_etree_iterparse  | 71.5 ms                                                    | 69.9 ms: 1.02x faster                                                      |
| xml_etree_parse      | 106 ms                                                     | 104 ms: 1.02x faster                                                       |
| pickle_dict          | 18.3 us                                                    | 18.1 us: 1.01x faster                                                      |
| pickle_list          | 2.96 us                                                    | 2.93 us: 1.01x faster                                                      |
| json_loads           | 16.8 us                                                    | 17.0 us: 1.01x slower                                                      |
| unpickle             | 9.12 us                                                    | 9.21 us: 1.01x slower                                                      |
| unpickle_list        | 2.88 us                                                    | 2.92 us: 1.01x slower                                                      |
| xml_etree_generate   | 52.7 ms                                                    | 53.3 ms: 1.01x slower                                                      |
| json_dumps           | 6.23 ms                                                    | 6.32 ms: 1.01x slower                                                      |
| pickle_pure_python   | 179 us                                                     | 181 us: 1.01x slower                                                       |
| Geometric mean       | (ref)                                                      | 1.02x faster                                                               |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240605-darwin-arm64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240502-darwin-arm64-brandtbucher-justin_trampolines-3.13.0a6+-6e8e3d5 |
|------------------------|:----------------------------------------------------------:|:--------------------------------------------------------------------------:|
| python_startup_no_site | 12.3 ms                                                    | 11.7 ms: 1.05x faster                                                      |
| python_startup         | 15.2 ms                                                    | 14.5 ms: 1.04x faster                                                      |
| Geometric mean         | (ref)                                                      | 1.05x faster                                                               |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240605-darwin-arm64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240502-darwin-arm64-brandtbucher-justin_trampolines-3.13.0a6+-6e8e3d5 |
|-----------------|:----------------------------------------------------------:|:--------------------------------------------------------------------------:|
| mako            | 6.99 ms                                                    | 6.39 ms: 1.09x faster                                                      |
| django_template | 19.4 ms                                                    | 21.2 ms: 1.09x slower                                                      |
| genshi_text     | 13.9 ms                                                    | 17.4 ms: 1.25x slower                                                      |
| genshi_xml      | 29.9 ms                                                    | 40.6 ms: 1.36x slower                                                      |
| Geometric mean  | (ref)                                                      | 1.14x slower                                                               |

All benchmarks:
===============

| Benchmark                        | bm-20240605-darwin-arm64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240502-darwin-arm64-brandtbucher-justin_trampolines-3.13.0a6+-6e8e3d5 |
|----------------------------------|:----------------------------------------------------------:|:--------------------------------------------------------------------------:|
| tomli_loads                      | 1.47 sec                                                   | 1.22 sec: 1.20x faster                                                     |
| mako                             | 6.99 ms                                                    | 6.39 ms: 1.09x faster                                                      |
| richards                         | 31.8 ms                                                    | 29.2 ms: 1.09x faster                                                      |
| unpickle_pure_python             | 141 us                                                     | 129 us: 1.09x faster                                                       |
| richards_super                   | 35.2 ms                                                    | 32.9 ms: 1.07x faster                                                      |
| fannkuch                         | 248 ms                                                     | 233 ms: 1.07x faster                                                       |
| python_startup_no_site           | 12.3 ms                                                    | 11.7 ms: 1.05x faster                                                      |
| async_tree_none                  | 209 ms                                                     | 200 ms: 1.05x faster                                                       |
| python_startup                   | 15.2 ms                                                    | 14.5 ms: 1.04x faster                                                      |
| pickle                           | 7.48 us                                                    | 7.20 us: 1.04x faster                                                      |
| xml_etree_process                | 37.1 ms                                                    | 35.7 ms: 1.04x faster                                                      |
| telco                            | 4.60 ms                                                    | 4.45 ms: 1.03x faster                                                      |
| pprint_safe_repr                 | 465 ms                                                     | 449 ms: 1.03x faster                                                       |
| pprint_pformat                   | 947 ms                                                     | 922 ms: 1.03x faster                                                       |
| xml_etree_iterparse              | 71.5 ms                                                    | 69.9 ms: 1.02x faster                                                      |
| pyflate                          | 321 ms                                                     | 314 ms: 1.02x faster                                                       |
| xml_etree_parse                  | 106 ms                                                     | 104 ms: 1.02x faster                                                       |
| crypto_pyaes                     | 49.5 ms                                                    | 48.7 ms: 1.02x faster                                                      |
| mdp                              | 1.53 sec                                                   | 1.52 sec: 1.01x faster                                                     |
| pickle_dict                      | 18.3 us                                                    | 18.1 us: 1.01x faster                                                      |
| pickle_list                      | 2.96 us                                                    | 2.93 us: 1.01x faster                                                      |
| html5lib                         | 31.2 ms                                                    | 30.9 ms: 1.01x faster                                                      |
| regex_effbot                     | 2.58 ms                                                    | 2.57 ms: 1.01x faster                                                      |
| asyncio_websockets               | 409 ms                                                     | 408 ms: 1.00x faster                                                       |
| gc_traversal                     | 2.45 ms                                                    | 2.46 ms: 1.00x slower                                                      |
| regex_v8                         | 17.3 ms                                                    | 17.3 ms: 1.00x slower                                                      |
| json_loads                       | 16.8 us                                                    | 17.0 us: 1.01x slower                                                      |
| coverage                         | 45.0 ms                                                    | 45.4 ms: 1.01x slower                                                      |
| unpickle                         | 9.12 us                                                    | 9.21 us: 1.01x slower                                                      |
| deepcopy_reduce                  | 1.82 us                                                    | 1.84 us: 1.01x slower                                                      |
| create_gc_cycles                 | 897 us                                                     | 906 us: 1.01x slower                                                       |
| unpickle_list                    | 2.88 us                                                    | 2.92 us: 1.01x slower                                                      |
| async_tree_eager_cpu_io_mixed_tg | 331 ms                                                     | 334 ms: 1.01x slower                                                       |
| xml_etree_generate               | 52.7 ms                                                    | 53.3 ms: 1.01x slower                                                      |
| json_dumps                       | 6.23 ms                                                    | 6.32 ms: 1.01x slower                                                      |
| pickle_pure_python               | 179 us                                                     | 181 us: 1.01x slower                                                       |
| float                            | 48.6 ms                                                    | 49.4 ms: 1.02x slower                                                      |
| sqlite_synth                     | 1.55 us                                                    | 1.58 us: 1.02x slower                                                      |
| async_tree_eager_cpu_io_mixed    | 358 ms                                                     | 365 ms: 1.02x slower                                                       |
| generators                       | 22.9 ms                                                    | 23.4 ms: 1.02x slower                                                      |
| pycparser                        | 632 ms                                                     | 646 ms: 1.02x slower                                                       |
| thrift                           | 435 us                                                     | 447 us: 1.03x slower                                                       |
| coroutines                       | 15.8 ms                                                    | 16.3 ms: 1.03x slower                                                      |
| logging_simple                   | 3.04 us                                                    | 3.13 us: 1.03x slower                                                      |
| asyncio_tcp_ssl                  | 1.29 sec                                                   | 1.33 sec: 1.03x slower                                                     |
| scimark_monte_carlo              | 42.5 ms                                                    | 43.7 ms: 1.03x slower                                                      |
| logging_format                   | 3.31 us                                                    | 3.41 us: 1.03x slower                                                      |
| meteor_contest                   | 70.3 ms                                                    | 72.5 ms: 1.03x slower                                                      |
| async_tree_cpu_io_mixed_tg       | 451 ms                                                     | 466 ms: 1.03x slower                                                       |
| deepcopy                         | 204 us                                                     | 211 us: 1.04x slower                                                       |
| async_generators                 | 281 ms                                                     | 291 ms: 1.04x slower                                                       |
| chameleon                        | 4.27 ms                                                    | 4.43 ms: 1.04x slower                                                      |
| deepcopy_memo                    | 22.6 us                                                    | 23.4 us: 1.04x slower                                                      |
| async_tree_eager_memoization_tg  | 126 ms                                                     | 130 ms: 1.04x slower                                                       |
| async_tree_eager_tg              | 41.4 ms                                                    | 43.1 ms: 1.04x slower                                                      |
| sympy_expand                     | 226 ms                                                     | 235 ms: 1.04x slower                                                       |
| sympy_str                        | 131 ms                                                     | 137 ms: 1.04x slower                                                       |
| regex_compile                    | 68.5 ms                                                    | 71.5 ms: 1.04x slower                                                      |
| docutils                         | 1.44 sec                                                   | 1.50 sec: 1.05x slower                                                     |
| go                               | 101 ms                                                     | 105 ms: 1.05x slower                                                       |
| sympy_sum                        | 69.2 ms                                                    | 72.6 ms: 1.05x slower                                                      |
| sqlglot_normalize                | 166 ms                                                     | 174 ms: 1.05x slower                                                       |
| dulwich_log                      | 27.6 ms                                                    | 29.0 ms: 1.05x slower                                                      |
| logging_silent                   | 60.1 ns                                                    | 63.2 ns: 1.05x slower                                                      |
| sympy_integrate                  | 10.3 ms                                                    | 10.9 ms: 1.06x slower                                                      |
| spectral_norm                    | 66.4 ms                                                    | 70.1 ms: 1.06x slower                                                      |
| 2to3                             | 161 ms                                                     | 170 ms: 1.06x slower                                                       |
| sqlglot_transpile                | 891 us                                                     | 943 us: 1.06x slower                                                       |
| sqlglot_parse                    | 732 us                                                     | 777 us: 1.06x slower                                                       |
| scimark_fft                      | 181 ms                                                     | 192 ms: 1.06x slower                                                       |
| sqlglot_optimize                 | 30.9 ms                                                    | 33.1 ms: 1.07x slower                                                      |
| async_tree_eager                 | 60.3 ms                                                    | 64.8 ms: 1.07x slower                                                      |
| hexiom                           | 4.06 ms                                                    | 4.36 ms: 1.08x slower                                                      |
| scimark_sparse_mat_mult          | 2.77 ms                                                    | 2.98 ms: 1.08x slower                                                      |
| async_tree_memoization_tg        | 240 ms                                                     | 258 ms: 1.08x slower                                                       |
| bench_thread_pool                | 447 us                                                     | 481 us: 1.08x slower                                                       |
| tornado_http                     | 66.7 ms                                                    | 72.1 ms: 1.08x slower                                                      |
| scimark_sor                      | 94.9 ms                                                    | 103 ms: 1.09x slower                                                       |
| django_template                  | 19.4 ms                                                    | 21.2 ms: 1.09x slower                                                      |
| nqueens                          | 52.2 ms                                                    | 57.5 ms: 1.10x slower                                                      |
| aiohttp                          | 997 us                                                     | 1.12 ms: 1.12x slower                                                      |
| deltablue                        | 2.14 ms                                                    | 2.41 ms: 1.12x slower                                                      |
| nbody                            | 59.6 ms                                                    | 67.8 ms: 1.14x slower                                                      |
| raytrace                         | 147 ms                                                     | 170 ms: 1.15x slower                                                       |
| gunicorn                         | 1.04 ms                                                    | 1.20 ms: 1.16x slower                                                      |
| typing_runtime_protocols         | 87.6 us                                                    | 102 us: 1.16x slower                                                       |
| chaos                            | 34.0 ms                                                    | 39.6 ms: 1.17x slower                                                      |
| scimark_lu                       | 66.9 ms                                                    | 78.8 ms: 1.18x slower                                                      |
| comprehensions                   | 10.2 us                                                    | 12.1 us: 1.20x slower                                                      |
| genshi_text                      | 13.9 ms                                                    | 17.4 ms: 1.25x slower                                                      |
| mypy2                            | 379 ms                                                     | 499 ms: 1.32x slower                                                       |
| genshi_xml                       | 29.9 ms                                                    | 40.6 ms: 1.36x slower                                                      |
| Geometric mean                   | (ref)                                                      | 1.03x slower                                                               |

Benchmark hidden because not significant (16): async_tree_eager_io_tg, async_tree_cpu_io_mixed, async_tree_io_tg, async_tree_io, async_tree_none_tg, bench_mp_pool, pathlib, regex_dna, pidigits, json, async_tree_eager_io, dask, async_tree_eager_memoization, async_tree_memoization, asyncio_tcp, pylint
Ignored benchmarks (2) of results/bm-20240605-3.13.0b2-3a83b17/bm-20240605-darwin-arm64-python-v3.13.0b2-3.13.0b2-3a83b17.json: bpe_tokeniser, flaskblogging

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.02x
- 95% likely to have a slowdown of 1.01x
- 99% likely to have a slowdown of 1.01x

# Memory
- memory change: 1.18x