# Results vs. 3.13.0b2

- fork: faster-cpython
- ref: no_thresholds
- machine: linux-x86_64
- commit hash: a4985b2
- commit date: 2024-03-28
- overall geometric mean: 1.03x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.01x slower
- Memory change: 1.06x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240328-linux-x86_64-faster%2dcpython-no_thresholds-3.13.0a5+-a4985b2 |
|----------------|:----------------------------------------------------------:|:-------------------------------------------------------------------------:|
| 2to3           | 274 ms                                                     | 281 ms: 1.02x slower                                                      |
| chameleon      | 7.22 ms                                                    | 7.06 ms: 1.02x faster                                                     |
| docutils       | 2.83 sec                                                   | 2.94 sec: 1.04x slower                                                    |
| html5lib       | 67.2 ms                                                    | 66.2 ms: 1.02x faster                                                     |
| tornado_http   | 94.6 ms                                                    | 97.6 ms: 1.03x slower                                                     |
| Geometric mean | (ref)                                                      | 1.01x slower                                                              |

Benchmarks with tag 'asyncio':
==============================

| Benchmark          | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240328-linux-x86_64-faster%2dcpython-no_thresholds-3.13.0a5+-a4985b2 |
|--------------------|:----------------------------------------------------------:|:-------------------------------------------------------------------------:|
| async_tree_none    | 378 ms                                                     | 355 ms: 1.07x faster                                                      |
| async_tree_none_tg | 336 ms                                                     | 347 ms: 1.03x slower                                                      |
| Geometric mean     | (ref)                                                      | 1.01x faster                                                              |

Benchmark hidden because not significant (6): async_tree_memoization, async_tree_io_tg, async_tree_io, async_tree_cpu_io_mixed, async_tree_memoization_tg, async_tree_cpu_io_mixed_tg

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240328-linux-x86_64-faster%2dcpython-no_thresholds-3.13.0a5+-a4985b2 |
|----------------|:----------------------------------------------------------:|:-------------------------------------------------------------------------:|
| pidigits       | 191 ms                                                     | 190 ms: 1.01x faster                                                      |
| float          | 78.9 ms                                                    | 79.5 ms: 1.01x slower                                                     |
| nbody          | 88.3 ms                                                    | 90.6 ms: 1.03x slower                                                     |
| Geometric mean | (ref)                                                      | 1.01x slower                                                              |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240328-linux-x86_64-faster%2dcpython-no_thresholds-3.13.0a5+-a4985b2 |
|----------------|:----------------------------------------------------------:|:-------------------------------------------------------------------------:|
| regex_effbot   | 3.67 ms                                                    | 3.81 ms: 1.04x slower                                                     |
| regex_v8       | 25.1 ms                                                    | 26.2 ms: 1.04x slower                                                     |
| regex_dna      | 221 ms                                                     | 231 ms: 1.04x slower                                                      |
| regex_compile  | 137 ms                                                     | 151 ms: 1.10x slower                                                      |
| Geometric mean | (ref)                                                      | 1.06x slower                                                              |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240328-linux-x86_64-faster%2dcpython-no_thresholds-3.13.0a5+-a4985b2 |
|----------------------|:----------------------------------------------------------:|:-------------------------------------------------------------------------:|
| unpickle_list        | 5.34 us                                                    | 5.04 us: 1.06x faster                                                     |
| pickle_list          | 5.11 us                                                    | 4.94 us: 1.03x faster                                                     |
| pickle_dict          | 34.8 us                                                    | 34.0 us: 1.02x faster                                                     |
| json_loads           | 28.9 us                                                    | 28.3 us: 1.02x faster                                                     |
| json_dumps           | 10.7 ms                                                    | 10.6 ms: 1.01x faster                                                     |
| pickle_pure_python   | 305 us                                                     | 306 us: 1.00x slower                                                      |
| tomli_loads          | 2.12 sec                                                   | 2.15 sec: 1.01x slower                                                    |
| xml_etree_process    | 61.2 ms                                                    | 62.8 ms: 1.03x slower                                                     |
| pickle               | 11.5 us                                                    | 11.9 us: 1.04x slower                                                     |
| xml_etree_generate   | 87.4 ms                                                    | 91.9 ms: 1.05x slower                                                     |
| xml_etree_iterparse  | 107 ms                                                     | 113 ms: 1.05x slower                                                      |
| unpickle             | 15.1 us                                                    | 16.7 us: 1.10x slower                                                     |
| unpickle_pure_python | 218 us                                                     | 267 us: 1.23x slower                                                      |
| Geometric mean       | (ref)                                                      | 1.02x slower                                                              |

Benchmark hidden because not significant (1): xml_etree_parse

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240328-linux-x86_64-faster%2dcpython-no_thresholds-3.13.0a5+-a4985b2 |
|------------------------|:----------------------------------------------------------:|:-------------------------------------------------------------------------:|
| python_startup         | 10.8 ms                                                    | 11.2 ms: 1.04x slower                                                     |
| python_startup_no_site | 7.11 ms                                                    | 9.62 ms: 1.35x slower                                                     |
| Geometric mean         | (ref)                                                      | 1.19x slower                                                              |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240328-linux-x86_64-faster%2dcpython-no_thresholds-3.13.0a5+-a4985b2 |
|-----------------|:----------------------------------------------------------:|:-------------------------------------------------------------------------:|
| mako            | 11.2 ms                                                    | 10.7 ms: 1.05x faster                                                     |
| django_template | 34.8 ms                                                    | 37.0 ms: 1.06x slower                                                     |
| genshi_text     | 23.7 ms                                                    | 25.9 ms: 1.09x slower                                                     |
| genshi_xml      | 51.6 ms                                                    | 57.0 ms: 1.10x slower                                                     |
| Geometric mean  | (ref)                                                      | 1.05x slower                                                              |

All benchmarks:
===============

| Benchmark                | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240328-linux-x86_64-faster%2dcpython-no_thresholds-3.13.0a5+-a4985b2 |
|--------------------------|:----------------------------------------------------------:|:-------------------------------------------------------------------------:|
| typing_runtime_protocols | 165 us                                                     | 116 us: 1.43x faster                                                      |
| scimark_fft              | 392 ms                                                     | 343 ms: 1.14x faster                                                      |
| scimark_sparse_mat_mult  | 5.27 ms                                                    | 4.79 ms: 1.10x faster                                                     |
| create_gc_cycles         | 1.82 ms                                                    | 1.70 ms: 1.07x faster                                                     |
| async_tree_none          | 378 ms                                                     | 355 ms: 1.07x faster                                                      |
| unpickle_list            | 5.34 us                                                    | 5.04 us: 1.06x faster                                                     |
| gc_traversal             | 3.98 ms                                                    | 3.77 ms: 1.06x faster                                                     |
| mako                     | 11.2 ms                                                    | 10.7 ms: 1.05x faster                                                     |
| sqlite_synth             | 2.99 us                                                    | 2.87 us: 1.04x faster                                                     |
| crypto_pyaes             | 77.5 ms                                                    | 74.9 ms: 1.03x faster                                                     |
| pickle_list              | 5.11 us                                                    | 4.94 us: 1.03x faster                                                     |
| pickle_dict              | 34.8 us                                                    | 34.0 us: 1.02x faster                                                     |
| chameleon                | 7.22 ms                                                    | 7.06 ms: 1.02x faster                                                     |
| json_loads               | 28.9 us                                                    | 28.3 us: 1.02x faster                                                     |
| deepcopy_reduce          | 3.35 us                                                    | 3.28 us: 1.02x faster                                                     |
| spectral_norm            | 116 ms                                                     | 114 ms: 1.02x faster                                                      |
| html5lib                 | 67.2 ms                                                    | 66.2 ms: 1.02x faster                                                     |
| json_dumps               | 10.7 ms                                                    | 10.6 ms: 1.01x faster                                                     |
| logging_silent           | 105 ns                                                     | 104 ns: 1.01x faster                                                      |
| pidigits                 | 191 ms                                                     | 190 ms: 1.01x faster                                                      |
| mdp                      | 2.79 sec                                                   | 2.77 sec: 1.01x faster                                                    |
| thrift                   | 823 us                                                     | 819 us: 1.00x faster                                                      |
| fannkuch                 | 402 ms                                                     | 400 ms: 1.00x faster                                                      |
| pickle_pure_python       | 305 us                                                     | 306 us: 1.00x slower                                                      |
| generators               | 29.6 ms                                                    | 29.8 ms: 1.00x slower                                                     |
| asyncio_websockets       | 567 ms                                                     | 570 ms: 1.01x slower                                                      |
| asyncio_tcp_ssl          | 1.84 sec                                                   | 1.85 sec: 1.01x slower                                                    |
| asyncio_tcp              | 508 ms                                                     | 512 ms: 1.01x slower                                                      |
| pyflate                  | 484 ms                                                     | 488 ms: 1.01x slower                                                      |
| float                    | 78.9 ms                                                    | 79.5 ms: 1.01x slower                                                     |
| tomli_loads              | 2.12 sec                                                   | 2.15 sec: 1.01x slower                                                    |
| pprint_pformat           | 1.56 sec                                                   | 1.58 sec: 1.02x slower                                                    |
| pprint_safe_repr         | 758 ms                                                     | 772 ms: 1.02x slower                                                      |
| dask                     | 369 ms                                                     | 376 ms: 1.02x slower                                                      |
| deepcopy                 | 367 us                                                     | 375 us: 1.02x slower                                                      |
| gunicorn                 | 1.28 ms                                                    | 1.30 ms: 1.02x slower                                                     |
| richards_super           | 57.4 ms                                                    | 58.6 ms: 1.02x slower                                                     |
| meteor_contest           | 110 ms                                                     | 112 ms: 1.02x slower                                                      |
| json                     | 5.31 ms                                                    | 5.43 ms: 1.02x slower                                                     |
| 2to3                     | 274 ms                                                     | 281 ms: 1.02x slower                                                      |
| nbody                    | 88.3 ms                                                    | 90.6 ms: 1.03x slower                                                     |
| aiohttp                  | 1.18 ms                                                    | 1.21 ms: 1.03x slower                                                     |
| xml_etree_process        | 61.2 ms                                                    | 62.8 ms: 1.03x slower                                                     |
| djangocms                | 31.5 us                                                    | 32.4 us: 1.03x slower                                                     |
| async_tree_none_tg       | 336 ms                                                     | 347 ms: 1.03x slower                                                      |
| sqlglot_transpile        | 1.63 ms                                                    | 1.69 ms: 1.03x slower                                                     |
| tornado_http             | 94.6 ms                                                    | 97.6 ms: 1.03x slower                                                     |
| telco                    | 8.41 ms                                                    | 8.68 ms: 1.03x slower                                                     |
| sqlglot_parse            | 1.32 ms                                                    | 1.36 ms: 1.03x slower                                                     |
| regex_effbot             | 3.67 ms                                                    | 3.81 ms: 1.04x slower                                                     |
| scimark_sor              | 127 ms                                                     | 132 ms: 1.04x slower                                                      |
| docutils                 | 2.83 sec                                                   | 2.94 sec: 1.04x slower                                                    |
| pickle                   | 11.5 us                                                    | 11.9 us: 1.04x slower                                                     |
| python_startup           | 10.8 ms                                                    | 11.2 ms: 1.04x slower                                                     |
| richards                 | 50.9 ms                                                    | 52.9 ms: 1.04x slower                                                     |
| logging_format           | 6.47 us                                                    | 6.73 us: 1.04x slower                                                     |
| sqlglot_normalize        | 110 ms                                                     | 115 ms: 1.04x slower                                                      |
| regex_v8                 | 25.1 ms                                                    | 26.2 ms: 1.04x slower                                                     |
| regex_dna                | 221 ms                                                     | 231 ms: 1.04x slower                                                      |
| sympy_str                | 282 ms                                                     | 295 ms: 1.04x slower                                                      |
| logging_simple           | 5.74 us                                                    | 6.01 us: 1.05x slower                                                     |
| coverage                 | 93.1 ms                                                    | 97.5 ms: 1.05x slower                                                     |
| xml_etree_generate       | 87.4 ms                                                    | 91.9 ms: 1.05x slower                                                     |
| xml_etree_iterparse      | 107 ms                                                     | 113 ms: 1.05x slower                                                      |
| sympy_expand             | 473 ms                                                     | 498 ms: 1.05x slower                                                      |
| django_template          | 34.8 ms                                                    | 37.0 ms: 1.06x slower                                                     |
| chaos                    | 61.3 ms                                                    | 65.3 ms: 1.06x slower                                                     |
| dulwich_log              | 67.2 ms                                                    | 71.5 ms: 1.06x slower                                                     |
| bench_thread_pool        | 834 us                                                     | 890 us: 1.07x slower                                                      |
| sqlglot_optimize         | 55.5 ms                                                    | 59.4 ms: 1.07x slower                                                     |
| pylint                   | 317 ms                                                     | 341 ms: 1.07x slower                                                      |
| mypy2                    | 742 ms                                                     | 798 ms: 1.08x slower                                                      |
| sympy_sum                | 156 ms                                                     | 168 ms: 1.08x slower                                                      |
| scimark_monte_carlo      | 69.2 ms                                                    | 74.8 ms: 1.08x slower                                                     |
| pycparser                | 1.16 sec                                                   | 1.26 sec: 1.09x slower                                                    |
| scimark_lu               | 122 ms                                                     | 132 ms: 1.09x slower                                                      |
| sympy_integrate          | 20.5 ms                                                    | 22.4 ms: 1.09x slower                                                     |
| genshi_text              | 23.7 ms                                                    | 25.9 ms: 1.09x slower                                                     |
| regex_compile            | 137 ms                                                     | 151 ms: 1.10x slower                                                      |
| genshi_xml               | 51.6 ms                                                    | 57.0 ms: 1.10x slower                                                     |
| unpickle                 | 15.1 us                                                    | 16.7 us: 1.10x slower                                                     |
| pathlib                  | 17.3 ms                                                    | 19.2 ms: 1.11x slower                                                     |
| async_generators         | 442 ms                                                     | 493 ms: 1.12x slower                                                      |
| deepcopy_memo            | 39.7 us                                                    | 44.9 us: 1.13x slower                                                     |
| raytrace                 | 267 ms                                                     | 302 ms: 1.13x slower                                                      |
| comprehensions           | 16.6 us                                                    | 19.5 us: 1.17x slower                                                     |
| go                       | 145 ms                                                     | 173 ms: 1.20x slower                                                      |
| unpickle_pure_python     | 218 us                                                     | 267 us: 1.23x slower                                                      |
| deltablue                | 3.25 ms                                                    | 4.14 ms: 1.27x slower                                                     |
| nqueens                  | 81.4 ms                                                    | 104 ms: 1.28x slower                                                      |
| hexiom                   | 6.30 ms                                                    | 8.09 ms: 1.29x slower                                                     |
| python_startup_no_site   | 7.11 ms                                                    | 9.62 ms: 1.35x slower                                                     |
| Geometric mean           | (ref)                                                      | 1.03x slower                                                              |

Benchmark hidden because not significant (9): async_tree_memoization, async_tree_io_tg, coroutines, async_tree_io, xml_etree_parse, async_tree_cpu_io_mixed, bench_mp_pool, async_tree_memoization_tg, async_tree_cpu_io_mixed_tg
Ignored benchmarks (2) of results/bm-20240605-3.13.0b2-3a83b17/bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17.json: bpe_tokeniser, flaskblogging
Ignored benchmarks (1) of results/bm-20240328-3.13.0a5+-a4985b2-JIT/bm-20240328-linux-x86_64-faster%2dcpython-no_thresholds-3.13.0a5+-a4985b2.json: unpack_sequence

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.01x
- 95% likely to have a slowdown of 1.01x
- 99% likely to have a slowdown of 1.01x

# Memory
- memory change: 1.06x