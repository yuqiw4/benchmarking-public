# Results vs. 3.13.0b2

- fork: brandtbucher
- ref: stitch_exhausted
- machine: darwin-arm64
- commit hash: 5a3dca4
- commit date: 2024-04-02
- overall geometric mean: 1.05x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.03x slower
- Memory change: 1.20x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240605-darwin-arm64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240402-darwin-arm64-brandtbucher-stitch_exhausted-3.13.0a5+-5a3dca4 |
|----------------|:----------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 161 ms                                                     | 176 ms: 1.09x slower                                                     |
| chameleon      | 4.27 ms                                                    | 4.47 ms: 1.05x slower                                                    |
| docutils       | 1.44 sec                                                   | 1.58 sec: 1.10x slower                                                   |
| html5lib       | 31.2 ms                                                    | 33.8 ms: 1.08x slower                                                    |
| tornado_http   | 66.7 ms                                                    | 82.2 ms: 1.23x slower                                                    |
| Geometric mean | (ref)                                                      | 1.11x slower                                                             |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240605-darwin-arm64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240402-darwin-arm64-brandtbucher-stitch_exhausted-3.13.0a5+-5a3dca4 |
|----------------------------------|:----------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_eager_io              | 766 ms                                                     | 735 ms: 1.04x faster                                                     |
| async_tree_eager_cpu_io_mixed    | 358 ms                                                     | 356 ms: 1.00x faster                                                     |
| async_tree_eager_cpu_io_mixed_tg | 331 ms                                                     | 336 ms: 1.02x slower                                                     |
| async_tree_cpu_io_mixed_tg       | 451 ms                                                     | 462 ms: 1.02x slower                                                     |
| async_tree_eager_memoization_tg  | 126 ms                                                     | 129 ms: 1.03x slower                                                     |
| async_tree_memoization_tg        | 240 ms                                                     | 249 ms: 1.04x slower                                                     |
| async_tree_eager_tg              | 41.4 ms                                                    | 44.8 ms: 1.08x slower                                                    |
| async_tree_none                  | 209 ms                                                     | 228 ms: 1.09x slower                                                     |
| async_tree_eager                 | 60.3 ms                                                    | 66.9 ms: 1.11x slower                                                    |
| Geometric mean                   | (ref)                                                      | 1.02x slower                                                             |

Benchmark hidden because not significant (7): async_tree_io_tg, async_tree_eager_io_tg, async_tree_cpu_io_mixed, async_tree_io, async_tree_none_tg, async_tree_eager_memoization, async_tree_memoization

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240605-darwin-arm64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240402-darwin-arm64-brandtbucher-stitch_exhausted-3.13.0a5+-5a3dca4 |
|----------------|:----------------------------------------------------------:|:------------------------------------------------------------------------:|
| pidigits       | 282 ms                                                     | 283 ms: 1.00x slower                                                     |
| float          | 48.6 ms                                                    | 49.2 ms: 1.01x slower                                                    |
| nbody          | 59.6 ms                                                    | 70.0 ms: 1.17x slower                                                    |
| Geometric mean | (ref)                                                      | 1.06x slower                                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240605-darwin-arm64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240402-darwin-arm64-brandtbucher-stitch_exhausted-3.13.0a5+-5a3dca4 |
|----------------|:----------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_v8       | 17.3 ms                                                    | 17.1 ms: 1.01x faster                                                    |
| regex_effbot   | 2.58 ms                                                    | 2.62 ms: 1.01x slower                                                    |
| regex_dna      | 149 ms                                                     | 152 ms: 1.02x slower                                                     |
| regex_compile  | 68.5 ms                                                    | 87.2 ms: 1.27x slower                                                    |
| Geometric mean | (ref)                                                      | 1.07x slower                                                             |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240605-darwin-arm64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240402-darwin-arm64-brandtbucher-stitch_exhausted-3.13.0a5+-5a3dca4 |
|----------------------|:----------------------------------------------------------:|:------------------------------------------------------------------------:|
| tomli_loads          | 1.47 sec                                                   | 1.29 sec: 1.14x faster                                                   |
| xml_etree_parse      | 106 ms                                                     | 98.3 ms: 1.07x faster                                                    |
| xml_etree_iterparse  | 71.5 ms                                                    | 68.5 ms: 1.04x faster                                                    |
| xml_etree_process    | 37.1 ms                                                    | 36.5 ms: 1.01x faster                                                    |
| pickle_dict          | 18.3 us                                                    | 18.0 us: 1.01x faster                                                    |
| pickle_list          | 2.96 us                                                    | 2.98 us: 1.01x slower                                                    |
| json_dumps           | 6.23 ms                                                    | 6.28 ms: 1.01x slower                                                    |
| json_loads           | 16.8 us                                                    | 17.1 us: 1.01x slower                                                    |
| unpickle_pure_python | 141 us                                                     | 143 us: 1.02x slower                                                     |
| pickle_pure_python   | 179 us                                                     | 183 us: 1.02x slower                                                     |
| xml_etree_generate   | 52.7 ms                                                    | 54.1 ms: 1.03x slower                                                    |
| unpickle_list        | 2.88 us                                                    | 3.04 us: 1.06x slower                                                    |
| Geometric mean       | (ref)                                                      | 1.01x faster                                                             |

Benchmark hidden because not significant (2): pickle, unpickle

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240605-darwin-arm64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240402-darwin-arm64-brandtbucher-stitch_exhausted-3.13.0a5+-5a3dca4 |
|------------------------|:----------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup         | 15.2 ms                                                    | 13.4 ms: 1.13x faster                                                    |
| python_startup_no_site | 12.3 ms                                                    | 11.6 ms: 1.06x faster                                                    |
| Geometric mean         | (ref)                                                      | 1.10x faster                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240605-darwin-arm64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240402-darwin-arm64-brandtbucher-stitch_exhausted-3.13.0a5+-5a3dca4 |
|-----------------|:----------------------------------------------------------:|:------------------------------------------------------------------------:|
| mako            | 6.99 ms                                                    | 6.96 ms: 1.00x faster                                                    |
| genshi_text     | 13.9 ms                                                    | 14.7 ms: 1.06x slower                                                    |
| genshi_xml      | 29.9 ms                                                    | 32.7 ms: 1.09x slower                                                    |
| django_template | 19.4 ms                                                    | 21.3 ms: 1.10x slower                                                    |
| Geometric mean  | (ref)                                                      | 1.06x slower                                                             |

All benchmarks:
===============

| Benchmark                        | bm-20240605-darwin-arm64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240402-darwin-arm64-brandtbucher-stitch_exhausted-3.13.0a5+-5a3dca4 |
|----------------------------------|:----------------------------------------------------------:|:------------------------------------------------------------------------:|
| typing_runtime_protocols         | 87.6 us                                                    | 69.9 us: 1.25x faster                                                    |
| tomli_loads                      | 1.47 sec                                                   | 1.29 sec: 1.14x faster                                                   |
| python_startup                   | 15.2 ms                                                    | 13.4 ms: 1.13x faster                                                    |
| xml_etree_parse                  | 106 ms                                                     | 98.3 ms: 1.07x faster                                                    |
| pylint                           | 170 ms                                                     | 159 ms: 1.07x faster                                                     |
| python_startup_no_site           | 12.3 ms                                                    | 11.6 ms: 1.06x faster                                                    |
| create_gc_cycles                 | 897 us                                                     | 847 us: 1.06x faster                                                     |
| xml_etree_iterparse              | 71.5 ms                                                    | 68.5 ms: 1.04x faster                                                    |
| async_tree_eager_io              | 766 ms                                                     | 735 ms: 1.04x faster                                                     |
| crypto_pyaes                     | 49.5 ms                                                    | 47.5 ms: 1.04x faster                                                    |
| telco                            | 4.60 ms                                                    | 4.48 ms: 1.03x faster                                                    |
| richards                         | 31.8 ms                                                    | 31.2 ms: 1.02x faster                                                    |
| xml_etree_process                | 37.1 ms                                                    | 36.5 ms: 1.01x faster                                                    |
| pickle_dict                      | 18.3 us                                                    | 18.0 us: 1.01x faster                                                    |
| richards_super                   | 35.2 ms                                                    | 34.8 ms: 1.01x faster                                                    |
| regex_v8                         | 17.3 ms                                                    | 17.1 ms: 1.01x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 358 ms                                                     | 356 ms: 1.00x faster                                                     |
| mako                             | 6.99 ms                                                    | 6.96 ms: 1.00x faster                                                    |
| gc_traversal                     | 2.45 ms                                                    | 2.45 ms: 1.00x faster                                                    |
| pidigits                         | 282 ms                                                     | 283 ms: 1.00x slower                                                     |
| thrift                           | 435 us                                                     | 437 us: 1.01x slower                                                     |
| json                             | 2.93 ms                                                    | 2.95 ms: 1.01x slower                                                    |
| pickle_list                      | 2.96 us                                                    | 2.98 us: 1.01x slower                                                    |
| json_dumps                       | 6.23 ms                                                    | 6.28 ms: 1.01x slower                                                    |
| float                            | 48.6 ms                                                    | 49.2 ms: 1.01x slower                                                    |
| json_loads                       | 16.8 us                                                    | 17.1 us: 1.01x slower                                                    |
| regex_effbot                     | 2.58 ms                                                    | 2.62 ms: 1.01x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 331 ms                                                     | 336 ms: 1.02x slower                                                     |
| unpickle_pure_python             | 141 us                                                     | 143 us: 1.02x slower                                                     |
| dask                             | 221 ms                                                     | 226 ms: 1.02x slower                                                     |
| regex_dna                        | 149 ms                                                     | 152 ms: 1.02x slower                                                     |
| sqlite_synth                     | 1.55 us                                                    | 1.58 us: 1.02x slower                                                    |
| pickle_pure_python               | 179 us                                                     | 183 us: 1.02x slower                                                     |
| async_tree_cpu_io_mixed_tg       | 451 ms                                                     | 462 ms: 1.02x slower                                                     |
| deepcopy_reduce                  | 1.82 us                                                    | 1.87 us: 1.03x slower                                                    |
| xml_etree_generate               | 52.7 ms                                                    | 54.1 ms: 1.03x slower                                                    |
| mdp                              | 1.53 sec                                                   | 1.58 sec: 1.03x slower                                                   |
| async_tree_eager_memoization_tg  | 126 ms                                                     | 129 ms: 1.03x slower                                                     |
| coverage                         | 45.0 ms                                                    | 46.4 ms: 1.03x slower                                                    |
| fannkuch                         | 248 ms                                                     | 258 ms: 1.04x slower                                                     |
| async_tree_memoization_tg        | 240 ms                                                     | 249 ms: 1.04x slower                                                     |
| pyflate                          | 321 ms                                                     | 335 ms: 1.04x slower                                                     |
| chameleon                        | 4.27 ms                                                    | 4.47 ms: 1.05x slower                                                    |
| sqlglot_parse                    | 732 us                                                     | 769 us: 1.05x slower                                                     |
| pycparser                        | 632 ms                                                     | 667 ms: 1.05x slower                                                     |
| deepcopy                         | 204 us                                                     | 215 us: 1.05x slower                                                     |
| coroutines                       | 15.8 ms                                                    | 16.7 ms: 1.06x slower                                                    |
| genshi_text                      | 13.9 ms                                                    | 14.7 ms: 1.06x slower                                                    |
| unpickle_list                    | 2.88 us                                                    | 3.04 us: 1.06x slower                                                    |
| meteor_contest                   | 70.3 ms                                                    | 74.4 ms: 1.06x slower                                                    |
| sqlglot_transpile                | 891 us                                                     | 944 us: 1.06x slower                                                     |
| pathlib                          | 23.3 ms                                                    | 24.7 ms: 1.06x slower                                                    |
| go                               | 101 ms                                                     | 107 ms: 1.07x slower                                                     |
| sympy_expand                     | 226 ms                                                     | 241 ms: 1.07x slower                                                     |
| async_generators                 | 281 ms                                                     | 301 ms: 1.07x slower                                                     |
| sqlglot_normalize                | 166 ms                                                     | 178 ms: 1.07x slower                                                     |
| deepcopy_memo                    | 22.6 us                                                    | 24.3 us: 1.08x slower                                                    |
| logging_simple                   | 3.04 us                                                    | 3.29 us: 1.08x slower                                                    |
| scimark_monte_carlo              | 42.5 ms                                                    | 45.9 ms: 1.08x slower                                                    |
| async_tree_eager_tg              | 41.4 ms                                                    | 44.8 ms: 1.08x slower                                                    |
| html5lib                         | 31.2 ms                                                    | 33.8 ms: 1.08x slower                                                    |
| logging_format                   | 3.31 us                                                    | 3.59 us: 1.09x slower                                                    |
| sympy_str                        | 131 ms                                                     | 143 ms: 1.09x slower                                                     |
| async_tree_none                  | 209 ms                                                     | 228 ms: 1.09x slower                                                     |
| genshi_xml                       | 29.9 ms                                                    | 32.7 ms: 1.09x slower                                                    |
| 2to3                             | 161 ms                                                     | 176 ms: 1.09x slower                                                     |
| logging_silent                   | 60.1 ns                                                    | 65.7 ns: 1.09x slower                                                    |
| dulwich_log                      | 27.6 ms                                                    | 30.2 ms: 1.10x slower                                                    |
| django_template                  | 19.4 ms                                                    | 21.3 ms: 1.10x slower                                                    |
| docutils                         | 1.44 sec                                                   | 1.58 sec: 1.10x slower                                                   |
| scimark_fft                      | 181 ms                                                     | 200 ms: 1.11x slower                                                     |
| deltablue                        | 2.14 ms                                                    | 2.37 ms: 1.11x slower                                                    |
| async_tree_eager                 | 60.3 ms                                                    | 66.9 ms: 1.11x slower                                                    |
| spectral_norm                    | 66.4 ms                                                    | 73.8 ms: 1.11x slower                                                    |
| sqlglot_optimize                 | 30.9 ms                                                    | 34.4 ms: 1.11x slower                                                    |
| asyncio_tcp                      | 402 ms                                                     | 449 ms: 1.12x slower                                                     |
| bench_thread_pool                | 447 us                                                     | 501 us: 1.12x slower                                                     |
| mypy2                            | 379 ms                                                     | 426 ms: 1.12x slower                                                     |
| sympy_sum                        | 69.2 ms                                                    | 77.9 ms: 1.13x slower                                                    |
| sympy_integrate                  | 10.3 ms                                                    | 11.7 ms: 1.13x slower                                                    |
| scimark_sparse_mat_mult          | 2.77 ms                                                    | 3.13 ms: 1.13x slower                                                    |
| pprint_pformat                   | 947 ms                                                     | 1.07 sec: 1.13x slower                                                   |
| scimark_sor                      | 94.9 ms                                                    | 108 ms: 1.13x slower                                                     |
| pprint_safe_repr                 | 465 ms                                                     | 527 ms: 1.13x slower                                                     |
| generators                       | 22.9 ms                                                    | 26.2 ms: 1.15x slower                                                    |
| aiohttp                          | 997 us                                                     | 1.14 ms: 1.15x slower                                                    |
| chaos                            | 34.0 ms                                                    | 39.4 ms: 1.16x slower                                                    |
| gunicorn                         | 1.04 ms                                                    | 1.21 ms: 1.16x slower                                                    |
| nbody                            | 59.6 ms                                                    | 70.0 ms: 1.17x slower                                                    |
| nqueens                          | 52.2 ms                                                    | 61.6 ms: 1.18x slower                                                    |
| comprehensions                   | 10.2 us                                                    | 12.1 us: 1.20x slower                                                    |
| scimark_lu                       | 66.9 ms                                                    | 81.5 ms: 1.22x slower                                                    |
| tornado_http                     | 66.7 ms                                                    | 82.2 ms: 1.23x slower                                                    |
| raytrace                         | 147 ms                                                     | 181 ms: 1.23x slower                                                     |
| regex_compile                    | 68.5 ms                                                    | 87.2 ms: 1.27x slower                                                    |
| hexiom                           | 4.06 ms                                                    | 5.28 ms: 1.30x slower                                                    |
| Geometric mean                   | (ref)                                                      | 1.05x slower                                                             |

Benchmark hidden because not significant (12): async_tree_io_tg, async_tree_eager_io_tg, bench_mp_pool, async_tree_cpu_io_mixed, pickle, asyncio_websockets, unpickle, asyncio_tcp_ssl, async_tree_io, async_tree_none_tg, async_tree_eager_memoization, async_tree_memoization
Ignored benchmarks (2) of results/bm-20240605-3.13.0b2-3a83b17/bm-20240605-darwin-arm64-python-v3.13.0b2-3.13.0b2-3a83b17.json: bpe_tokeniser, flaskblogging
Ignored benchmarks (1) of results/bm-20240402-3.13.0a5+-5a3dca4-JIT/bm-20240402-darwin-arm64-brandtbucher-stitch_exhausted-3.13.0a5+-5a3dca4.json: unpack_sequence

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.04x
- 95% likely to have a slowdown of 1.04x
- 99% likely to have a slowdown of 1.03x

# Memory
- memory change: 1.20x