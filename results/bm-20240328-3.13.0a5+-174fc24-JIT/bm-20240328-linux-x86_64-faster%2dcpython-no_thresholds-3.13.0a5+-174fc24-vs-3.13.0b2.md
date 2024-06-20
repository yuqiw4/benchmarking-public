# Results vs. 3.13.0b2

- fork: faster-cpython
- ref: no_thresholds
- machine: linux-x86_64
- commit hash: 174fc24
- commit date: 2024-03-28
- overall geometric mean: 1.04x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.01x slower
- Memory change: 1.06x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240328-linux-x86_64-faster%2dcpython-no_thresholds-3.13.0a5+-174fc24 |
|----------------|:----------------------------------------------------------:|:-------------------------------------------------------------------------:|
| 2to3           | 274 ms                                                     | 280 ms: 1.02x slower                                                      |
| docutils       | 2.83 sec                                                   | 2.93 sec: 1.04x slower                                                    |
| html5lib       | 67.2 ms                                                    | 66.4 ms: 1.01x faster                                                     |
| tornado_http   | 94.6 ms                                                    | 96.9 ms: 1.02x slower                                                     |
| Geometric mean | (ref)                                                      | 1.01x slower                                                              |

Benchmark hidden because not significant (1): chameleon

Benchmarks with tag 'asyncio':
==============================

| Benchmark          | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240328-linux-x86_64-faster%2dcpython-no_thresholds-3.13.0a5+-174fc24 |
|--------------------|:----------------------------------------------------------:|:-------------------------------------------------------------------------:|
| async_tree_none    | 378 ms                                                     | 360 ms: 1.05x faster                                                      |
| async_tree_io_tg   | 936 ms                                                     | 909 ms: 1.03x faster                                                      |
| async_tree_none_tg | 336 ms                                                     | 348 ms: 1.03x slower                                                      |
| Geometric mean     | (ref)                                                      | 1.01x faster                                                              |

Benchmark hidden because not significant (5): async_tree_memoization, async_tree_io, async_tree_cpu_io_mixed, async_tree_memoization_tg, async_tree_cpu_io_mixed_tg

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240328-linux-x86_64-faster%2dcpython-no_thresholds-3.13.0a5+-174fc24 |
|----------------|:----------------------------------------------------------:|:-------------------------------------------------------------------------:|
| pidigits       | 191 ms                                                     | 189 ms: 1.01x faster                                                      |
| float          | 78.9 ms                                                    | 79.6 ms: 1.01x slower                                                     |
| nbody          | 88.3 ms                                                    | 92.7 ms: 1.05x slower                                                     |
| Geometric mean | (ref)                                                      | 1.02x slower                                                              |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240328-linux-x86_64-faster%2dcpython-no_thresholds-3.13.0a5+-174fc24 |
|----------------|:----------------------------------------------------------:|:-------------------------------------------------------------------------:|
| regex_v8       | 25.1 ms                                                    | 25.7 ms: 1.02x slower                                                     |
| regex_effbot   | 3.67 ms                                                    | 3.78 ms: 1.03x slower                                                     |
| regex_dna      | 221 ms                                                     | 234 ms: 1.06x slower                                                      |
| regex_compile  | 137 ms                                                     | 151 ms: 1.11x slower                                                      |
| Geometric mean | (ref)                                                      | 1.05x slower                                                              |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240328-linux-x86_64-faster%2dcpython-no_thresholds-3.13.0a5+-174fc24 |
|----------------------|:----------------------------------------------------------:|:-------------------------------------------------------------------------:|
| unpickle_list        | 5.34 us                                                    | 5.19 us: 1.03x faster                                                     |
| json_loads           | 28.9 us                                                    | 28.6 us: 1.01x faster                                                     |
| pickle_list          | 5.11 us                                                    | 5.12 us: 1.00x slower                                                     |
| tomli_loads          | 2.12 sec                                                   | 2.13 sec: 1.01x slower                                                    |
| pickle_pure_python   | 305 us                                                     | 309 us: 1.01x slower                                                      |
| xml_etree_process    | 61.2 ms                                                    | 62.6 ms: 1.02x slower                                                     |
| xml_etree_iterparse  | 107 ms                                                     | 112 ms: 1.05x slower                                                      |
| pickle_dict          | 34.8 us                                                    | 36.5 us: 1.05x slower                                                     |
| pickle               | 11.5 us                                                    | 12.1 us: 1.06x slower                                                     |
| xml_etree_generate   | 87.4 ms                                                    | 92.9 ms: 1.06x slower                                                     |
| unpickle             | 15.1 us                                                    | 17.1 us: 1.13x slower                                                     |
| unpickle_pure_python | 218 us                                                     | 268 us: 1.23x slower                                                      |
| Geometric mean       | (ref)                                                      | 1.04x slower                                                              |

Benchmark hidden because not significant (2): xml_etree_parse, json_dumps

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240328-linux-x86_64-faster%2dcpython-no_thresholds-3.13.0a5+-174fc24 |
|------------------------|:----------------------------------------------------------:|:-------------------------------------------------------------------------:|
| python_startup         | 10.8 ms                                                    | 11.1 ms: 1.03x slower                                                     |
| python_startup_no_site | 7.11 ms                                                    | 9.54 ms: 1.34x slower                                                     |
| Geometric mean         | (ref)                                                      | 1.18x slower                                                              |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240328-linux-x86_64-faster%2dcpython-no_thresholds-3.13.0a5+-174fc24 |
|-----------------|:----------------------------------------------------------:|:-------------------------------------------------------------------------:|
| mako            | 11.2 ms                                                    | 10.8 ms: 1.04x faster                                                     |
| django_template | 34.8 ms                                                    | 37.1 ms: 1.07x slower                                                     |
| genshi_text     | 23.7 ms                                                    | 25.8 ms: 1.09x slower                                                     |
| genshi_xml      | 51.6 ms                                                    | 57.3 ms: 1.11x slower                                                     |
| Geometric mean  | (ref)                                                      | 1.05x slower                                                              |

All benchmarks:
===============

| Benchmark                | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240328-linux-x86_64-faster%2dcpython-no_thresholds-3.13.0a5+-174fc24 |
|--------------------------|:----------------------------------------------------------:|:-------------------------------------------------------------------------:|
| typing_runtime_protocols | 165 us                                                     | 116 us: 1.42x faster                                                      |
| scimark_fft              | 392 ms                                                     | 342 ms: 1.15x faster                                                      |
| scimark_sparse_mat_mult  | 5.27 ms                                                    | 4.84 ms: 1.09x faster                                                     |
| create_gc_cycles         | 1.82 ms                                                    | 1.69 ms: 1.07x faster                                                     |
| async_tree_none          | 378 ms                                                     | 360 ms: 1.05x faster                                                      |
| gc_traversal             | 3.98 ms                                                    | 3.78 ms: 1.05x faster                                                     |
| mako                     | 11.2 ms                                                    | 10.8 ms: 1.04x faster                                                     |
| sqlite_synth             | 2.99 us                                                    | 2.88 us: 1.04x faster                                                     |
| unpickle_list            | 5.34 us                                                    | 5.19 us: 1.03x faster                                                     |
| async_tree_io_tg         | 936 ms                                                     | 909 ms: 1.03x faster                                                      |
| coroutines               | 23.2 ms                                                    | 22.6 ms: 1.02x faster                                                     |
| crypto_pyaes             | 77.5 ms                                                    | 75.6 ms: 1.02x faster                                                     |
| deepcopy_reduce          | 3.35 us                                                    | 3.27 us: 1.02x faster                                                     |
| spectral_norm            | 116 ms                                                     | 114 ms: 1.02x faster                                                      |
| mdp                      | 2.79 sec                                                   | 2.75 sec: 1.01x faster                                                    |
| html5lib                 | 67.2 ms                                                    | 66.4 ms: 1.01x faster                                                     |
| json_loads               | 28.9 us                                                    | 28.6 us: 1.01x faster                                                     |
| pidigits                 | 191 ms                                                     | 189 ms: 1.01x faster                                                      |
| pickle_list              | 5.11 us                                                    | 5.12 us: 1.00x slower                                                     |
| asyncio_websockets       | 567 ms                                                     | 570 ms: 1.01x slower                                                      |
| tomli_loads              | 2.12 sec                                                   | 2.13 sec: 1.01x slower                                                    |
| asyncio_tcp              | 508 ms                                                     | 511 ms: 1.01x slower                                                      |
| deepcopy                 | 367 us                                                     | 370 us: 1.01x slower                                                      |
| pyflate                  | 484 ms                                                     | 488 ms: 1.01x slower                                                      |
| float                    | 78.9 ms                                                    | 79.6 ms: 1.01x slower                                                     |
| asyncio_tcp_ssl          | 1.84 sec                                                   | 1.86 sec: 1.01x slower                                                    |
| generators               | 29.6 ms                                                    | 29.9 ms: 1.01x slower                                                     |
| pprint_safe_repr         | 758 ms                                                     | 767 ms: 1.01x slower                                                      |
| pickle_pure_python       | 305 us                                                     | 309 us: 1.01x slower                                                      |
| meteor_contest           | 110 ms                                                     | 111 ms: 1.01x slower                                                      |
| logging_silent           | 105 ns                                                     | 106 ns: 1.01x slower                                                      |
| fannkuch                 | 402 ms                                                     | 410 ms: 1.02x slower                                                      |
| 2to3                     | 274 ms                                                     | 280 ms: 1.02x slower                                                      |
| xml_etree_process        | 61.2 ms                                                    | 62.6 ms: 1.02x slower                                                     |
| djangocms                | 31.5 us                                                    | 32.2 us: 1.02x slower                                                     |
| regex_v8                 | 25.1 ms                                                    | 25.7 ms: 1.02x slower                                                     |
| dask                     | 369 ms                                                     | 378 ms: 1.02x slower                                                      |
| tornado_http             | 94.6 ms                                                    | 96.9 ms: 1.02x slower                                                     |
| aiohttp                  | 1.18 ms                                                    | 1.21 ms: 1.03x slower                                                     |
| pprint_pformat           | 1.56 sec                                                   | 1.60 sec: 1.03x slower                                                    |
| gunicorn                 | 1.28 ms                                                    | 1.31 ms: 1.03x slower                                                     |
| python_startup           | 10.8 ms                                                    | 11.1 ms: 1.03x slower                                                     |
| regex_effbot             | 3.67 ms                                                    | 3.78 ms: 1.03x slower                                                     |
| json                     | 5.31 ms                                                    | 5.47 ms: 1.03x slower                                                     |
| async_tree_none_tg       | 336 ms                                                     | 348 ms: 1.03x slower                                                      |
| docutils                 | 2.83 sec                                                   | 2.93 sec: 1.04x slower                                                    |
| scimark_sor              | 127 ms                                                     | 132 ms: 1.04x slower                                                      |
| logging_format           | 6.47 us                                                    | 6.71 us: 1.04x slower                                                     |
| sqlglot_normalize        | 110 ms                                                     | 114 ms: 1.04x slower                                                      |
| sqlglot_parse            | 1.32 ms                                                    | 1.37 ms: 1.04x slower                                                     |
| richards_super           | 57.4 ms                                                    | 59.7 ms: 1.04x slower                                                     |
| sqlglot_transpile        | 1.63 ms                                                    | 1.71 ms: 1.05x slower                                                     |
| xml_etree_iterparse      | 107 ms                                                     | 112 ms: 1.05x slower                                                      |
| sympy_str                | 282 ms                                                     | 296 ms: 1.05x slower                                                      |
| nbody                    | 88.3 ms                                                    | 92.7 ms: 1.05x slower                                                     |
| coverage                 | 93.1 ms                                                    | 97.8 ms: 1.05x slower                                                     |
| pickle_dict              | 34.8 us                                                    | 36.5 us: 1.05x slower                                                     |
| telco                    | 8.41 ms                                                    | 8.85 ms: 1.05x slower                                                     |
| logging_simple           | 5.74 us                                                    | 6.07 us: 1.06x slower                                                     |
| pickle                   | 11.5 us                                                    | 12.1 us: 1.06x slower                                                     |
| sympy_expand             | 473 ms                                                     | 500 ms: 1.06x slower                                                      |
| regex_dna                | 221 ms                                                     | 234 ms: 1.06x slower                                                      |
| richards                 | 50.9 ms                                                    | 54.0 ms: 1.06x slower                                                     |
| xml_etree_generate       | 87.4 ms                                                    | 92.9 ms: 1.06x slower                                                     |
| chaos                    | 61.3 ms                                                    | 65.4 ms: 1.07x slower                                                     |
| django_template          | 34.8 ms                                                    | 37.1 ms: 1.07x slower                                                     |
| bench_thread_pool        | 834 us                                                     | 890 us: 1.07x slower                                                      |
| dulwich_log              | 67.2 ms                                                    | 71.8 ms: 1.07x slower                                                     |
| sqlglot_optimize         | 55.5 ms                                                    | 59.5 ms: 1.07x slower                                                     |
| pylint                   | 317 ms                                                     | 340 ms: 1.07x slower                                                      |
| sympy_sum                | 156 ms                                                     | 167 ms: 1.07x slower                                                      |
| mypy2                    | 742 ms                                                     | 801 ms: 1.08x slower                                                      |
| pycparser                | 1.16 sec                                                   | 1.25 sec: 1.08x slower                                                    |
| scimark_lu               | 122 ms                                                     | 132 ms: 1.09x slower                                                      |
| scimark_monte_carlo      | 69.2 ms                                                    | 75.3 ms: 1.09x slower                                                     |
| genshi_text              | 23.7 ms                                                    | 25.8 ms: 1.09x slower                                                     |
| sympy_integrate          | 20.5 ms                                                    | 22.4 ms: 1.09x slower                                                     |
| regex_compile            | 137 ms                                                     | 151 ms: 1.11x slower                                                      |
| genshi_xml               | 51.6 ms                                                    | 57.3 ms: 1.11x slower                                                     |
| pathlib                  | 17.3 ms                                                    | 19.4 ms: 1.12x slower                                                     |
| deepcopy_memo            | 39.7 us                                                    | 44.8 us: 1.13x slower                                                     |
| unpickle                 | 15.1 us                                                    | 17.1 us: 1.13x slower                                                     |
| async_generators         | 442 ms                                                     | 502 ms: 1.14x slower                                                      |
| raytrace                 | 267 ms                                                     | 303 ms: 1.14x slower                                                      |
| comprehensions           | 16.6 us                                                    | 19.4 us: 1.17x slower                                                     |
| go                       | 145 ms                                                     | 175 ms: 1.21x slower                                                      |
| unpickle_pure_python     | 218 us                                                     | 268 us: 1.23x slower                                                      |
| deltablue                | 3.25 ms                                                    | 4.15 ms: 1.28x slower                                                     |
| hexiom                   | 6.30 ms                                                    | 8.12 ms: 1.29x slower                                                     |
| nqueens                  | 81.4 ms                                                    | 109 ms: 1.34x slower                                                      |
| python_startup_no_site   | 7.11 ms                                                    | 9.54 ms: 1.34x slower                                                     |
| Geometric mean           | (ref)                                                      | 1.04x slower                                                              |

Benchmark hidden because not significant (10): xml_etree_parse, async_tree_memoization, chameleon, async_tree_io, json_dumps, thrift, async_tree_cpu_io_mixed, bench_mp_pool, async_tree_memoization_tg, async_tree_cpu_io_mixed_tg
Ignored benchmarks (2) of results/bm-20240605-3.13.0b2-3a83b17/bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17.json: bpe_tokeniser, flaskblogging
Ignored benchmarks (1) of results/bm-20240328-3.13.0a5+-174fc24-JIT/bm-20240328-linux-x86_64-faster%2dcpython-no_thresholds-3.13.0a5+-174fc24.json: unpack_sequence

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.02x
- 95% likely to have a slowdown of 1.01x
- 99% likely to have a slowdown of 1.01x

# Memory
- memory change: 1.06x