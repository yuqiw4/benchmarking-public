# Results vs. 3.13.0b2

- fork: brandtbucher
- ref: justin_ghccc
- machine: darwin-arm64
- commit hash: eeeedaf
- commit date: 2024-03-30
- overall geometric mean: 1.04x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.03x slower
- Memory change: 1.17x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240605-darwin-arm64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240330-darwin-arm64-brandtbucher-justin_ghccc-3.13.0a5+-eeeedaf |
|----------------|:----------------------------------------------------------:|:--------------------------------------------------------------------:|
| 2to3           | 161 ms                                                     | 174 ms: 1.08x slower                                                 |
| chameleon      | 4.27 ms                                                    | 4.55 ms: 1.07x slower                                                |
| docutils       | 1.44 sec                                                   | 1.55 sec: 1.08x slower                                               |
| html5lib       | 31.2 ms                                                    | 33.5 ms: 1.08x slower                                                |
| tornado_http   | 66.7 ms                                                    | 77.9 ms: 1.17x slower                                                |
| Geometric mean | (ref)                                                      | 1.09x slower                                                         |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240605-darwin-arm64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240330-darwin-arm64-brandtbucher-justin_ghccc-3.13.0a5+-eeeedaf |
|----------------------------------|:----------------------------------------------------------:|:--------------------------------------------------------------------:|
| async_tree_eager_io              | 766 ms                                                     | 735 ms: 1.04x faster                                                 |
| async_tree_eager_cpu_io_mixed    | 358 ms                                                     | 355 ms: 1.01x faster                                                 |
| async_tree_eager_cpu_io_mixed_tg | 331 ms                                                     | 336 ms: 1.01x slower                                                 |
| async_tree_eager_memoization_tg  | 126 ms                                                     | 129 ms: 1.03x slower                                                 |
| async_tree_memoization_tg        | 240 ms                                                     | 249 ms: 1.04x slower                                                 |
| async_tree_eager_tg              | 41.4 ms                                                    | 44.7 ms: 1.08x slower                                                |
| async_tree_none                  | 209 ms                                                     | 228 ms: 1.09x slower                                                 |
| async_tree_eager                 | 60.3 ms                                                    | 65.8 ms: 1.09x slower                                                |
| Geometric mean                   | (ref)                                                      | 1.02x slower                                                         |

Benchmark hidden because not significant (8): async_tree_io_tg, async_tree_cpu_io_mixed, async_tree_eager_io_tg, async_tree_io, async_tree_eager_memoization, async_tree_none_tg, async_tree_cpu_io_mixed_tg, async_tree_memoization

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240605-darwin-arm64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240330-darwin-arm64-brandtbucher-justin_ghccc-3.13.0a5+-eeeedaf |
|----------------|:----------------------------------------------------------:|:--------------------------------------------------------------------:|
| pidigits       | 282 ms                                                     | 282 ms: 1.00x slower                                                 |
| float          | 48.6 ms                                                    | 49.3 ms: 1.01x slower                                                |
| nbody          | 59.6 ms                                                    | 70.2 ms: 1.18x slower                                                |
| Geometric mean | (ref)                                                      | 1.06x slower                                                         |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240605-darwin-arm64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240330-darwin-arm64-brandtbucher-justin_ghccc-3.13.0a5+-eeeedaf |
|----------------|:----------------------------------------------------------:|:--------------------------------------------------------------------:|
| regex_v8       | 17.3 ms                                                    | 17.1 ms: 1.01x faster                                                |
| regex_effbot   | 2.58 ms                                                    | 2.62 ms: 1.01x slower                                                |
| regex_dna      | 149 ms                                                     | 152 ms: 1.02x slower                                                 |
| regex_compile  | 68.5 ms                                                    | 80.9 ms: 1.18x slower                                                |
| Geometric mean | (ref)                                                      | 1.05x slower                                                         |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240605-darwin-arm64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240330-darwin-arm64-brandtbucher-justin_ghccc-3.13.0a5+-eeeedaf |
|----------------------|:----------------------------------------------------------:|:--------------------------------------------------------------------:|
| tomli_loads          | 1.47 sec                                                   | 1.29 sec: 1.14x faster                                               |
| pickle_dict          | 18.3 us                                                    | 18.0 us: 1.01x faster                                                |
| pickle               | 7.48 us                                                    | 7.40 us: 1.01x faster                                                |
| xml_etree_process    | 37.1 ms                                                    | 36.8 ms: 1.01x faster                                                |
| pickle_list          | 2.96 us                                                    | 2.98 us: 1.01x slower                                                |
| json_loads           | 16.8 us                                                    | 17.0 us: 1.01x slower                                                |
| xml_etree_iterparse  | 71.5 ms                                                    | 72.5 ms: 1.01x slower                                                |
| json_dumps           | 6.23 ms                                                    | 6.34 ms: 1.02x slower                                                |
| unpickle_pure_python | 141 us                                                     | 143 us: 1.02x slower                                                 |
| pickle_pure_python   | 179 us                                                     | 183 us: 1.02x slower                                                 |
| xml_etree_generate   | 52.7 ms                                                    | 54.2 ms: 1.03x slower                                                |
| unpickle_list        | 2.88 us                                                    | 3.08 us: 1.07x slower                                                |
| Geometric mean       | (ref)                                                      | 1.00x slower                                                         |

Benchmark hidden because not significant (2): unpickle, xml_etree_parse

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240605-darwin-arm64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240330-darwin-arm64-brandtbucher-justin_ghccc-3.13.0a5+-eeeedaf |
|------------------------|:----------------------------------------------------------:|:--------------------------------------------------------------------:|
| python_startup         | 15.2 ms                                                    | 13.4 ms: 1.13x faster                                                |
| python_startup_no_site | 12.3 ms                                                    | 11.6 ms: 1.06x faster                                                |
| Geometric mean         | (ref)                                                      | 1.10x faster                                                         |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240605-darwin-arm64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240330-darwin-arm64-brandtbucher-justin_ghccc-3.13.0a5+-eeeedaf |
|-----------------|:----------------------------------------------------------:|:--------------------------------------------------------------------:|
| mako            | 6.99 ms                                                    | 6.94 ms: 1.01x faster                                                |
| genshi_xml      | 29.9 ms                                                    | 31.2 ms: 1.04x slower                                                |
| genshi_text     | 13.9 ms                                                    | 14.8 ms: 1.06x slower                                                |
| django_template | 19.4 ms                                                    | 20.8 ms: 1.07x slower                                                |
| Geometric mean  | (ref)                                                      | 1.04x slower                                                         |

All benchmarks:
===============

| Benchmark                        | bm-20240605-darwin-arm64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240330-darwin-arm64-brandtbucher-justin_ghccc-3.13.0a5+-eeeedaf |
|----------------------------------|:----------------------------------------------------------:|:--------------------------------------------------------------------:|
| typing_runtime_protocols         | 87.6 us                                                    | 69.6 us: 1.26x faster                                                |
| tomli_loads                      | 1.47 sec                                                   | 1.29 sec: 1.14x faster                                               |
| python_startup                   | 15.2 ms                                                    | 13.4 ms: 1.13x faster                                                |
| pylint                           | 170 ms                                                     | 156 ms: 1.09x faster                                                 |
| python_startup_no_site           | 12.3 ms                                                    | 11.6 ms: 1.06x faster                                                |
| create_gc_cycles                 | 897 us                                                     | 846 us: 1.06x faster                                                 |
| crypto_pyaes                     | 49.5 ms                                                    | 47.1 ms: 1.05x faster                                                |
| async_tree_eager_io              | 766 ms                                                     | 735 ms: 1.04x faster                                                 |
| bench_mp_pool                    | 47.2 ms                                                    | 46.5 ms: 1.01x faster                                                |
| pickle_dict                      | 18.3 us                                                    | 18.0 us: 1.01x faster                                                |
| regex_v8                         | 17.3 ms                                                    | 17.1 ms: 1.01x faster                                                |
| pickle                           | 7.48 us                                                    | 7.40 us: 1.01x faster                                                |
| async_tree_eager_cpu_io_mixed    | 358 ms                                                     | 355 ms: 1.01x faster                                                 |
| xml_etree_process                | 37.1 ms                                                    | 36.8 ms: 1.01x faster                                                |
| richards                         | 31.8 ms                                                    | 31.6 ms: 1.01x faster                                                |
| mako                             | 6.99 ms                                                    | 6.94 ms: 1.01x faster                                                |
| telco                            | 4.60 ms                                                    | 4.59 ms: 1.00x faster                                                |
| gc_traversal                     | 2.45 ms                                                    | 2.45 ms: 1.00x faster                                                |
| pidigits                         | 282 ms                                                     | 282 ms: 1.00x slower                                                 |
| richards_super                   | 35.2 ms                                                    | 35.3 ms: 1.00x slower                                                |
| thrift                           | 435 us                                                     | 438 us: 1.01x slower                                                 |
| pickle_list                      | 2.96 us                                                    | 2.98 us: 1.01x slower                                                |
| json_loads                       | 16.8 us                                                    | 17.0 us: 1.01x slower                                                |
| float                            | 48.6 ms                                                    | 49.3 ms: 1.01x slower                                                |
| xml_etree_iterparse              | 71.5 ms                                                    | 72.5 ms: 1.01x slower                                                |
| regex_effbot                     | 2.58 ms                                                    | 2.62 ms: 1.01x slower                                                |
| async_tree_eager_cpu_io_mixed_tg | 331 ms                                                     | 336 ms: 1.01x slower                                                 |
| json_dumps                       | 6.23 ms                                                    | 6.34 ms: 1.02x slower                                                |
| unpickle_pure_python             | 141 us                                                     | 143 us: 1.02x slower                                                 |
| sqlite_synth                     | 1.55 us                                                    | 1.58 us: 1.02x slower                                                |
| regex_dna                        | 149 ms                                                     | 152 ms: 1.02x slower                                                 |
| asyncio_tcp_ssl                  | 1.29 sec                                                   | 1.32 sec: 1.02x slower                                               |
| json                             | 2.93 ms                                                    | 2.99 ms: 1.02x slower                                                |
| pickle_pure_python               | 179 us                                                     | 183 us: 1.02x slower                                                 |
| async_tree_eager_memoization_tg  | 126 ms                                                     | 129 ms: 1.03x slower                                                 |
| xml_etree_generate               | 52.7 ms                                                    | 54.2 ms: 1.03x slower                                                |
| deepcopy_reduce                  | 1.82 us                                                    | 1.88 us: 1.03x slower                                                |
| mdp                              | 1.53 sec                                                   | 1.58 sec: 1.03x slower                                               |
| pyflate                          | 321 ms                                                     | 331 ms: 1.03x slower                                                 |
| go                               | 101 ms                                                     | 104 ms: 1.04x slower                                                 |
| async_tree_memoization_tg        | 240 ms                                                     | 249 ms: 1.04x slower                                                 |
| coverage                         | 45.0 ms                                                    | 46.9 ms: 1.04x slower                                                |
| meteor_contest                   | 70.3 ms                                                    | 73.3 ms: 1.04x slower                                                |
| genshi_xml                       | 29.9 ms                                                    | 31.2 ms: 1.04x slower                                                |
| pprint_safe_repr                 | 465 ms                                                     | 485 ms: 1.04x slower                                                 |
| pprint_pformat                   | 947 ms                                                     | 991 ms: 1.05x slower                                                 |
| scimark_monte_carlo              | 42.5 ms                                                    | 44.5 ms: 1.05x slower                                                |
| sqlglot_parse                    | 732 us                                                     | 767 us: 1.05x slower                                                 |
| sympy_expand                     | 226 ms                                                     | 237 ms: 1.05x slower                                                 |
| deepcopy                         | 204 us                                                     | 215 us: 1.05x slower                                                 |
| pycparser                        | 632 ms                                                     | 665 ms: 1.05x slower                                                 |
| sqlglot_transpile                | 891 us                                                     | 937 us: 1.05x slower                                                 |
| fannkuch                         | 248 ms                                                     | 263 ms: 1.06x slower                                                 |
| sqlglot_normalize                | 166 ms                                                     | 176 ms: 1.06x slower                                                 |
| sympy_str                        | 131 ms                                                     | 140 ms: 1.06x slower                                                 |
| coroutines                       | 15.8 ms                                                    | 16.8 ms: 1.06x slower                                                |
| genshi_text                      | 13.9 ms                                                    | 14.8 ms: 1.06x slower                                                |
| chameleon                        | 4.27 ms                                                    | 4.55 ms: 1.07x slower                                                |
| unpickle_list                    | 2.88 us                                                    | 3.08 us: 1.07x slower                                                |
| django_template                  | 19.4 ms                                                    | 20.8 ms: 1.07x slower                                                |
| pathlib                          | 23.3 ms                                                    | 25.0 ms: 1.07x slower                                                |
| html5lib                         | 31.2 ms                                                    | 33.5 ms: 1.08x slower                                                |
| deepcopy_memo                    | 22.6 us                                                    | 24.3 us: 1.08x slower                                                |
| docutils                         | 1.44 sec                                                   | 1.55 sec: 1.08x slower                                               |
| async_generators                 | 281 ms                                                     | 303 ms: 1.08x slower                                                 |
| 2to3                             | 161 ms                                                     | 174 ms: 1.08x slower                                                 |
| async_tree_eager_tg              | 41.4 ms                                                    | 44.7 ms: 1.08x slower                                                |
| logging_format                   | 3.31 us                                                    | 3.58 us: 1.08x slower                                                |
| logging_simple                   | 3.04 us                                                    | 3.29 us: 1.08x slower                                                |
| mypy2                            | 379 ms                                                     | 411 ms: 1.08x slower                                                 |
| async_tree_none                  | 209 ms                                                     | 228 ms: 1.09x slower                                                 |
| dulwich_log                      | 27.6 ms                                                    | 30.0 ms: 1.09x slower                                                |
| async_tree_eager                 | 60.3 ms                                                    | 65.8 ms: 1.09x slower                                                |
| sqlglot_optimize                 | 30.9 ms                                                    | 33.7 ms: 1.09x slower                                                |
| sympy_integrate                  | 10.3 ms                                                    | 11.3 ms: 1.09x slower                                                |
| logging_silent                   | 60.1 ns                                                    | 65.8 ns: 1.09x slower                                                |
| sympy_sum                        | 69.2 ms                                                    | 75.9 ms: 1.10x slower                                                |
| scimark_fft                      | 181 ms                                                     | 199 ms: 1.10x slower                                                 |
| deltablue                        | 2.14 ms                                                    | 2.36 ms: 1.10x slower                                                |
| bench_thread_pool                | 447 us                                                     | 494 us: 1.11x slower                                                 |
| spectral_norm                    | 66.4 ms                                                    | 73.6 ms: 1.11x slower                                                |
| aiohttp                          | 997 us                                                     | 1.12 ms: 1.12x slower                                                |
| scimark_sparse_mat_mult          | 2.77 ms                                                    | 3.13 ms: 1.13x slower                                                |
| scimark_sor                      | 94.9 ms                                                    | 107 ms: 1.13x slower                                                 |
| chaos                            | 34.0 ms                                                    | 38.7 ms: 1.14x slower                                                |
| generators                       | 22.9 ms                                                    | 26.4 ms: 1.15x slower                                                |
| gunicorn                         | 1.04 ms                                                    | 1.20 ms: 1.15x slower                                                |
| nqueens                          | 52.2 ms                                                    | 60.4 ms: 1.16x slower                                                |
| tornado_http                     | 66.7 ms                                                    | 77.9 ms: 1.17x slower                                                |
| nbody                            | 59.6 ms                                                    | 70.2 ms: 1.18x slower                                                |
| regex_compile                    | 68.5 ms                                                    | 80.9 ms: 1.18x slower                                                |
| comprehensions                   | 10.2 us                                                    | 12.1 us: 1.19x slower                                                |
| hexiom                           | 4.06 ms                                                    | 4.95 ms: 1.22x slower                                                |
| raytrace                         | 147 ms                                                     | 180 ms: 1.22x slower                                                 |
| scimark_lu                       | 66.9 ms                                                    | 82.0 ms: 1.23x slower                                                |
| Geometric mean                   | (ref)                                                      | 1.04x slower                                                         |

Benchmark hidden because not significant (13): async_tree_io_tg, async_tree_cpu_io_mixed, asyncio_tcp, dask, asyncio_websockets, async_tree_eager_io_tg, unpickle, async_tree_io, xml_etree_parse, async_tree_eager_memoization, async_tree_none_tg, async_tree_cpu_io_mixed_tg, async_tree_memoization
Ignored benchmarks (2) of results/bm-20240605-3.13.0b2-3a83b17/bm-20240605-darwin-arm64-python-v3.13.0b2-3.13.0b2-3a83b17.json: bpe_tokeniser, flaskblogging
Ignored benchmarks (1) of results/bm-20240330-3.13.0a5+-eeeedaf-JIT/bm-20240330-darwin-arm64-brandtbucher-justin_ghccc-3.13.0a5+-eeeedaf.json: unpack_sequence

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.03x
- 95% likely to have a slowdown of 1.03x
- 99% likely to have a slowdown of 1.03x

# Memory
- memory change: 1.17x