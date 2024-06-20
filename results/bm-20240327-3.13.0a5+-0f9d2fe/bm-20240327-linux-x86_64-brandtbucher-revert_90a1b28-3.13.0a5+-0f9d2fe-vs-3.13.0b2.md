# Results vs. 3.13.0b2

- fork: brandtbucher
- ref: revert_90a1b28
- machine: linux-x86_64
- commit hash: 0f9d2fe
- commit date: 2024-03-27
- overall geometric mean: 1.02x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.00x faster
- Memory change: 0.97x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240327-linux-x86_64-brandtbucher-revert_90a1b28-3.13.0a5+-0f9d2fe |
|----------------|:----------------------------------------------------------:|:----------------------------------------------------------------------:|
| 2to3           | 274 ms                                                     | 267 ms: 1.03x faster                                                   |
| chameleon      | 7.22 ms                                                    | 6.95 ms: 1.04x faster                                                  |
| docutils       | 2.83 sec                                                   | 2.76 sec: 1.02x faster                                                 |
| html5lib       | 67.2 ms                                                    | 65.7 ms: 1.02x faster                                                  |
| tornado_http   | 94.6 ms                                                    | 95.0 ms: 1.00x slower                                                  |
| Geometric mean | (ref)                                                      | 1.02x faster                                                           |

Benchmarks with tag 'asyncio':
==============================

| Benchmark              | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240327-linux-x86_64-brandtbucher-revert_90a1b28-3.13.0a5+-0f9d2fe |
|------------------------|:----------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_memoization | 463 ms                                                     | 442 ms: 1.05x faster                                                   |
| async_tree_io_tg       | 936 ms                                                     | 898 ms: 1.04x faster                                                   |
| Geometric mean         | (ref)                                                      | 1.02x faster                                                           |

Benchmark hidden because not significant (6): async_tree_none, async_tree_io, async_tree_memoization_tg, async_tree_cpu_io_mixed, async_tree_cpu_io_mixed_tg, async_tree_none_tg

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240327-linux-x86_64-brandtbucher-revert_90a1b28-3.13.0a5+-0f9d2fe |
|----------------|:----------------------------------------------------------:|:----------------------------------------------------------------------:|
| float          | 78.9 ms                                                    | 76.7 ms: 1.03x faster                                                  |
| pidigits       | 191 ms                                                     | 190 ms: 1.01x faster                                                   |
| nbody          | 88.3 ms                                                    | 90.2 ms: 1.02x slower                                                  |
| Geometric mean | (ref)                                                      | 1.01x faster                                                           |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240327-linux-x86_64-brandtbucher-revert_90a1b28-3.13.0a5+-0f9d2fe |
|----------------|:----------------------------------------------------------:|:----------------------------------------------------------------------:|
| regex_compile  | 137 ms                                                     | 134 ms: 1.02x faster                                                   |
| regex_effbot   | 3.67 ms                                                    | 3.71 ms: 1.01x slower                                                  |
| regex_dna      | 221 ms                                                     | 225 ms: 1.02x slower                                                   |
| regex_v8       | 25.1 ms                                                    | 25.6 ms: 1.02x slower                                                  |
| Geometric mean | (ref)                                                      | 1.01x slower                                                           |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240327-linux-x86_64-brandtbucher-revert_90a1b28-3.13.0a5+-0f9d2fe |
|----------------------|:----------------------------------------------------------:|:----------------------------------------------------------------------:|
| unpickle_list        | 5.34 us                                                    | 5.16 us: 1.04x faster                                                  |
| xml_etree_process    | 61.2 ms                                                    | 59.2 ms: 1.03x faster                                                  |
| pickle_list          | 5.11 us                                                    | 4.97 us: 1.03x faster                                                  |
| json_dumps           | 10.7 ms                                                    | 10.5 ms: 1.02x faster                                                  |
| pickle_pure_python   | 305 us                                                     | 299 us: 1.02x faster                                                   |
| xml_etree_generate   | 87.4 ms                                                    | 85.8 ms: 1.02x faster                                                  |
| pickle_dict          | 34.8 us                                                    | 34.3 us: 1.01x faster                                                  |
| xml_etree_iterparse  | 107 ms                                                     | 106 ms: 1.01x faster                                                   |
| unpickle             | 15.1 us                                                    | 14.9 us: 1.01x faster                                                  |
| pickle               | 11.5 us                                                    | 11.7 us: 1.02x slower                                                  |
| unpickle_pure_python | 218 us                                                     | 222 us: 1.02x slower                                                   |
| tomli_loads          | 2.12 sec                                                   | 2.17 sec: 1.02x slower                                                 |
| Geometric mean       | (ref)                                                      | 1.01x faster                                                           |

Benchmark hidden because not significant (2): xml_etree_parse, json_loads

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240327-linux-x86_64-brandtbucher-revert_90a1b28-3.13.0a5+-0f9d2fe |
|------------------------|:----------------------------------------------------------:|:----------------------------------------------------------------------:|
| python_startup         | 10.8 ms                                                    | 10.4 ms: 1.03x faster                                                  |
| python_startup_no_site | 7.11 ms                                                    | 6.89 ms: 1.03x faster                                                  |
| Geometric mean         | (ref)                                                      | 1.03x faster                                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240327-linux-x86_64-brandtbucher-revert_90a1b28-3.13.0a5+-0f9d2fe |
|-----------------|:----------------------------------------------------------:|:----------------------------------------------------------------------:|
| mako            | 11.2 ms                                                    | 10.9 ms: 1.03x faster                                                  |
| django_template | 34.8 ms                                                    | 34.2 ms: 1.02x faster                                                  |
| genshi_text     | 23.7 ms                                                    | 24.5 ms: 1.04x slower                                                  |
| Geometric mean  | (ref)                                                      | 1.00x faster                                                           |

Benchmark hidden because not significant (1): genshi_xml

All benchmarks:
===============

| Benchmark                | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240327-linux-x86_64-brandtbucher-revert_90a1b28-3.13.0a5+-0f9d2fe |
|--------------------------|:----------------------------------------------------------:|:----------------------------------------------------------------------:|
| typing_runtime_protocols | 165 us                                                     | 112 us: 1.47x faster                                                   |
| richards_super           | 57.4 ms                                                    | 52.2 ms: 1.10x faster                                                  |
| richards                 | 50.9 ms                                                    | 46.3 ms: 1.10x faster                                                  |
| scimark_sparse_mat_mult  | 5.27 ms                                                    | 4.80 ms: 1.10x faster                                                  |
| create_gc_cycles         | 1.82 ms                                                    | 1.67 ms: 1.09x faster                                                  |
| mdp                      | 2.79 sec                                                   | 2.57 sec: 1.08x faster                                                 |
| scimark_fft              | 392 ms                                                     | 366 ms: 1.07x faster                                                   |
| spectral_norm            | 116 ms                                                     | 108 ms: 1.07x faster                                                   |
| scimark_lu               | 122 ms                                                     | 115 ms: 1.06x faster                                                   |
| deepcopy_reduce          | 3.35 us                                                    | 3.17 us: 1.06x faster                                                  |
| crypto_pyaes             | 77.5 ms                                                    | 73.4 ms: 1.06x faster                                                  |
| async_tree_memoization   | 463 ms                                                     | 442 ms: 1.05x faster                                                   |
| pyflate                  | 484 ms                                                     | 463 ms: 1.05x faster                                                   |
| deepcopy                 | 367 us                                                     | 352 us: 1.04x faster                                                   |
| async_tree_io_tg         | 936 ms                                                     | 898 ms: 1.04x faster                                                   |
| scimark_sor              | 127 ms                                                     | 123 ms: 1.04x faster                                                   |
| sqlglot_transpile        | 1.63 ms                                                    | 1.57 ms: 1.04x faster                                                  |
| chameleon                | 7.22 ms                                                    | 6.95 ms: 1.04x faster                                                  |
| sqlglot_parse            | 1.32 ms                                                    | 1.27 ms: 1.04x faster                                                  |
| unpickle_list            | 5.34 us                                                    | 5.16 us: 1.04x faster                                                  |
| python_startup           | 10.8 ms                                                    | 10.4 ms: 1.03x faster                                                  |
| logging_silent           | 105 ns                                                     | 101 ns: 1.03x faster                                                   |
| sympy_str                | 282 ms                                                     | 273 ms: 1.03x faster                                                   |
| xml_etree_process        | 61.2 ms                                                    | 59.2 ms: 1.03x faster                                                  |
| pprint_pformat           | 1.56 sec                                                   | 1.51 sec: 1.03x faster                                                 |
| python_startup_no_site   | 7.11 ms                                                    | 6.89 ms: 1.03x faster                                                  |
| pprint_safe_repr         | 758 ms                                                     | 735 ms: 1.03x faster                                                   |
| mako                     | 11.2 ms                                                    | 10.9 ms: 1.03x faster                                                  |
| deepcopy_memo            | 39.7 us                                                    | 38.5 us: 1.03x faster                                                  |
| float                    | 78.9 ms                                                    | 76.7 ms: 1.03x faster                                                  |
| 2to3                     | 274 ms                                                     | 267 ms: 1.03x faster                                                   |
| pickle_list              | 5.11 us                                                    | 4.97 us: 1.03x faster                                                  |
| json_dumps               | 10.7 ms                                                    | 10.5 ms: 1.02x faster                                                  |
| docutils                 | 2.83 sec                                                   | 2.76 sec: 1.02x faster                                                 |
| sympy_sum                | 156 ms                                                     | 152 ms: 1.02x faster                                                   |
| coroutines               | 23.2 ms                                                    | 22.7 ms: 1.02x faster                                                  |
| html5lib                 | 67.2 ms                                                    | 65.7 ms: 1.02x faster                                                  |
| pickle_pure_python       | 305 us                                                     | 299 us: 1.02x faster                                                   |
| sympy_expand             | 473 ms                                                     | 462 ms: 1.02x faster                                                   |
| go                       | 145 ms                                                     | 141 ms: 1.02x faster                                                   |
| scimark_monte_carlo      | 69.2 ms                                                    | 67.7 ms: 1.02x faster                                                  |
| sqlite_synth             | 2.99 us                                                    | 2.93 us: 1.02x faster                                                  |
| thrift                   | 823 us                                                     | 806 us: 1.02x faster                                                   |
| asyncio_tcp              | 508 ms                                                     | 498 ms: 1.02x faster                                                   |
| fannkuch                 | 402 ms                                                     | 394 ms: 1.02x faster                                                   |
| sympy_integrate          | 20.5 ms                                                    | 20.1 ms: 1.02x faster                                                  |
| xml_etree_generate       | 87.4 ms                                                    | 85.8 ms: 1.02x faster                                                  |
| regex_compile            | 137 ms                                                     | 134 ms: 1.02x faster                                                   |
| chaos                    | 61.3 ms                                                    | 60.2 ms: 1.02x faster                                                  |
| django_template          | 34.8 ms                                                    | 34.2 ms: 1.02x faster                                                  |
| sqlglot_optimize         | 55.5 ms                                                    | 54.7 ms: 1.02x faster                                                  |
| pickle_dict              | 34.8 us                                                    | 34.3 us: 1.01x faster                                                  |
| nqueens                  | 81.4 ms                                                    | 80.3 ms: 1.01x faster                                                  |
| xml_etree_iterparse      | 107 ms                                                     | 106 ms: 1.01x faster                                                   |
| unpickle                 | 15.1 us                                                    | 14.9 us: 1.01x faster                                                  |
| sqlglot_normalize        | 110 ms                                                     | 109 ms: 1.01x faster                                                   |
| meteor_contest           | 110 ms                                                     | 109 ms: 1.01x faster                                                   |
| comprehensions           | 16.6 us                                                    | 16.5 us: 1.01x faster                                                  |
| pidigits                 | 191 ms                                                     | 190 ms: 1.01x faster                                                   |
| aiohttp                  | 1.18 ms                                                    | 1.17 ms: 1.01x faster                                                  |
| bench_thread_pool        | 834 us                                                     | 831 us: 1.00x faster                                                   |
| asyncio_tcp_ssl          | 1.84 sec                                                   | 1.84 sec: 1.00x faster                                                 |
| tornado_http             | 94.6 ms                                                    | 95.0 ms: 1.00x slower                                                  |
| dulwich_log              | 67.2 ms                                                    | 67.5 ms: 1.00x slower                                                  |
| async_generators         | 442 ms                                                     | 445 ms: 1.01x slower                                                   |
| gc_traversal             | 3.98 ms                                                    | 4.00 ms: 1.01x slower                                                  |
| regex_effbot             | 3.67 ms                                                    | 3.71 ms: 1.01x slower                                                  |
| logging_format           | 6.47 us                                                    | 6.54 us: 1.01x slower                                                  |
| regex_dna                | 221 ms                                                     | 225 ms: 1.02x slower                                                   |
| pickle                   | 11.5 us                                                    | 11.7 us: 1.02x slower                                                  |
| unpickle_pure_python     | 218 us                                                     | 222 us: 1.02x slower                                                   |
| pycparser                | 1.16 sec                                                   | 1.18 sec: 1.02x slower                                                 |
| regex_v8                 | 25.1 ms                                                    | 25.6 ms: 1.02x slower                                                  |
| tomli_loads              | 2.12 sec                                                   | 2.17 sec: 1.02x slower                                                 |
| nbody                    | 88.3 ms                                                    | 90.2 ms: 1.02x slower                                                  |
| coverage                 | 93.1 ms                                                    | 95.5 ms: 1.03x slower                                                  |
| genshi_text              | 23.7 ms                                                    | 24.5 ms: 1.04x slower                                                  |
| logging_simple           | 5.74 us                                                    | 5.95 us: 1.04x slower                                                  |
| pathlib                  | 17.3 ms                                                    | 18.4 ms: 1.06x slower                                                  |
| Geometric mean           | (ref)                                                      | 1.02x faster                                                           |

Benchmark hidden because not significant (22): async_tree_none, async_tree_io, async_tree_memoization_tg, xml_etree_parse, mypy2, dask, json_loads, async_tree_cpu_io_mixed, bench_mp_pool, deltablue, raytrace, async_tree_cpu_io_mixed_tg, hexiom, gunicorn, generators, pylint, genshi_xml, asyncio_websockets, json, telco, djangocms, async_tree_none_tg
Ignored benchmarks (2) of results/bm-20240605-3.13.0b2-3a83b17/bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17.json: bpe_tokeniser, flaskblogging
Ignored benchmarks (1) of results/bm-20240327-3.13.0a5+-0f9d2fe/bm-20240327-linux-x86_64-brandtbucher-revert_90a1b28-3.13.0a5+-0f9d2fe.json: unpack_sequence

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.01x
- 95% likely to have a speedup of 1.01x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 0.97x