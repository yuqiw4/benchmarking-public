# Results vs. 3.13.0b2

- fork: brandtbucher
- ref: stitch_exhausted
- machine: linux-x86_64
- commit hash: 5a3dca4
- commit date: 2024-04-02
- overall geometric mean: 1.01x slower
- HPT reliability: 99.96%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.07x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240402-linux-x86_64-brandtbucher-stitch_exhausted-3.13.0a5+-5a3dca4 |
|----------------|:----------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 274 ms                                                     | 282 ms: 1.03x slower                                                     |
| chameleon      | 7.22 ms                                                    | 7.06 ms: 1.02x faster                                                    |
| docutils       | 2.83 sec                                                   | 2.94 sec: 1.04x slower                                                   |
| html5lib       | 67.2 ms                                                    | 67.6 ms: 1.01x slower                                                    |
| tornado_http   | 94.6 ms                                                    | 96.5 ms: 1.02x slower                                                    |
| Geometric mean | (ref)                                                      | 1.01x slower                                                             |

Benchmarks with tag 'asyncio':
==============================

| Benchmark          | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240402-linux-x86_64-brandtbucher-stitch_exhausted-3.13.0a5+-5a3dca4 |
|--------------------|:----------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_none    | 378 ms                                                     | 357 ms: 1.06x faster                                                     |
| async_tree_io_tg   | 936 ms                                                     | 907 ms: 1.03x faster                                                     |
| async_tree_none_tg | 336 ms                                                     | 348 ms: 1.03x slower                                                     |
| Geometric mean     | (ref)                                                      | 1.01x faster                                                             |

Benchmark hidden because not significant (5): async_tree_memoization, async_tree_io, async_tree_cpu_io_mixed, async_tree_memoization_tg, async_tree_cpu_io_mixed_tg

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240402-linux-x86_64-brandtbucher-stitch_exhausted-3.13.0a5+-5a3dca4 |
|----------------|:----------------------------------------------------------:|:------------------------------------------------------------------------:|
| float          | 78.9 ms                                                    | 77.0 ms: 1.03x faster                                                    |
| pidigits       | 191 ms                                                     | 189 ms: 1.01x faster                                                     |
| nbody          | 88.3 ms                                                    | 92.4 ms: 1.05x slower                                                    |
| Geometric mean | (ref)                                                      | 1.00x slower                                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240402-linux-x86_64-brandtbucher-stitch_exhausted-3.13.0a5+-5a3dca4 |
|----------------|:----------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_v8       | 25.1 ms                                                    | 24.7 ms: 1.02x faster                                                    |
| regex_effbot   | 3.67 ms                                                    | 3.75 ms: 1.02x slower                                                    |
| regex_compile  | 137 ms                                                     | 149 ms: 1.09x slower                                                     |
| Geometric mean | (ref)                                                      | 1.02x slower                                                             |

Benchmark hidden because not significant (1): regex_dna

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240402-linux-x86_64-brandtbucher-stitch_exhausted-3.13.0a5+-5a3dca4 |
|----------------------|:----------------------------------------------------------:|:------------------------------------------------------------------------:|
| tomli_loads          | 2.12 sec                                                   | 2.06 sec: 1.03x faster                                                   |
| unpickle_list        | 5.34 us                                                    | 5.19 us: 1.03x faster                                                    |
| pickle_list          | 5.11 us                                                    | 4.96 us: 1.03x faster                                                    |
| xml_etree_process    | 61.2 ms                                                    | 59.8 ms: 1.02x faster                                                    |
| pickle_dict          | 34.8 us                                                    | 34.1 us: 1.02x faster                                                    |
| xml_etree_generate   | 87.4 ms                                                    | 86.7 ms: 1.01x faster                                                    |
| pickle_pure_python   | 305 us                                                     | 308 us: 1.01x slower                                                     |
| pickle               | 11.5 us                                                    | 11.8 us: 1.02x slower                                                    |
| unpickle_pure_python | 218 us                                                     | 238 us: 1.09x slower                                                     |
| Geometric mean       | (ref)                                                      | 1.00x faster                                                             |

Benchmark hidden because not significant (5): xml_etree_parse, unpickle, xml_etree_iterparse, json_dumps, json_loads

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240402-linux-x86_64-brandtbucher-stitch_exhausted-3.13.0a5+-5a3dca4 |
|------------------------|:----------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup         | 10.8 ms                                                    | 11.1 ms: 1.03x slower                                                    |
| python_startup_no_site | 7.11 ms                                                    | 9.51 ms: 1.34x slower                                                    |
| Geometric mean         | (ref)                                                      | 1.17x slower                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240402-linux-x86_64-brandtbucher-stitch_exhausted-3.13.0a5+-5a3dca4 |
|-----------------|:----------------------------------------------------------:|:------------------------------------------------------------------------:|
| mako            | 11.2 ms                                                    | 11.0 ms: 1.02x faster                                                    |
| genshi_text     | 23.7 ms                                                    | 24.8 ms: 1.05x slower                                                    |
| django_template | 34.8 ms                                                    | 37.1 ms: 1.07x slower                                                    |
| genshi_xml      | 51.6 ms                                                    | 55.7 ms: 1.08x slower                                                    |
| Geometric mean  | (ref)                                                      | 1.04x slower                                                             |

All benchmarks:
===============

| Benchmark                | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240402-linux-x86_64-brandtbucher-stitch_exhausted-3.13.0a5+-5a3dca4 |
|--------------------------|:----------------------------------------------------------:|:------------------------------------------------------------------------:|
| typing_runtime_protocols | 165 us                                                     | 114 us: 1.45x faster                                                     |
| scimark_fft              | 392 ms                                                     | 343 ms: 1.14x faster                                                     |
| richards                 | 50.9 ms                                                    | 46.4 ms: 1.10x faster                                                    |
| richards_super           | 57.4 ms                                                    | 53.0 ms: 1.08x faster                                                    |
| scimark_sparse_mat_mult  | 5.27 ms                                                    | 4.87 ms: 1.08x faster                                                    |
| create_gc_cycles         | 1.82 ms                                                    | 1.68 ms: 1.08x faster                                                    |
| async_tree_none          | 378 ms                                                     | 357 ms: 1.06x faster                                                     |
| deepcopy_reduce          | 3.35 us                                                    | 3.18 us: 1.05x faster                                                    |
| sqlite_synth             | 2.99 us                                                    | 2.86 us: 1.04x faster                                                    |
| async_tree_io_tg         | 936 ms                                                     | 907 ms: 1.03x faster                                                     |
| fannkuch                 | 402 ms                                                     | 390 ms: 1.03x faster                                                     |
| tomli_loads              | 2.12 sec                                                   | 2.06 sec: 1.03x faster                                                   |
| unpickle_list            | 5.34 us                                                    | 5.19 us: 1.03x faster                                                    |
| pickle_list              | 5.11 us                                                    | 4.96 us: 1.03x faster                                                    |
| crypto_pyaes             | 77.5 ms                                                    | 75.3 ms: 1.03x faster                                                    |
| float                    | 78.9 ms                                                    | 77.0 ms: 1.03x faster                                                    |
| mako                     | 11.2 ms                                                    | 11.0 ms: 1.02x faster                                                    |
| xml_etree_process        | 61.2 ms                                                    | 59.8 ms: 1.02x faster                                                    |
| chameleon                | 7.22 ms                                                    | 7.06 ms: 1.02x faster                                                    |
| deepcopy                 | 367 us                                                     | 359 us: 1.02x faster                                                     |
| logging_silent           | 105 ns                                                     | 103 ns: 1.02x faster                                                     |
| pickle_dict              | 34.8 us                                                    | 34.1 us: 1.02x faster                                                    |
| spectral_norm            | 116 ms                                                     | 114 ms: 1.02x faster                                                     |
| regex_v8                 | 25.1 ms                                                    | 24.7 ms: 1.02x faster                                                    |
| coroutines               | 23.2 ms                                                    | 22.8 ms: 1.02x faster                                                    |
| deepcopy_memo            | 39.7 us                                                    | 39.3 us: 1.01x faster                                                    |
| thrift                   | 823 us                                                     | 814 us: 1.01x faster                                                     |
| pidigits                 | 191 ms                                                     | 189 ms: 1.01x faster                                                     |
| logging_format           | 6.47 us                                                    | 6.42 us: 1.01x faster                                                    |
| xml_etree_generate       | 87.4 ms                                                    | 86.7 ms: 1.01x faster                                                    |
| gc_traversal             | 3.98 ms                                                    | 3.99 ms: 1.00x slower                                                    |
| bench_mp_pool            | 23.9 ms                                                    | 24.0 ms: 1.01x slower                                                    |
| html5lib                 | 67.2 ms                                                    | 67.6 ms: 1.01x slower                                                    |
| pickle_pure_python       | 305 us                                                     | 308 us: 1.01x slower                                                     |
| asyncio_tcp_ssl          | 1.84 sec                                                   | 1.86 sec: 1.01x slower                                                   |
| mdp                      | 2.79 sec                                                   | 2.82 sec: 1.01x slower                                                   |
| pyflate                  | 484 ms                                                     | 491 ms: 1.01x slower                                                     |
| generators               | 29.6 ms                                                    | 30.1 ms: 1.01x slower                                                    |
| meteor_contest           | 110 ms                                                     | 111 ms: 1.01x slower                                                     |
| logging_simple           | 5.74 us                                                    | 5.84 us: 1.02x slower                                                    |
| asyncio_tcp              | 508 ms                                                     | 518 ms: 1.02x slower                                                     |
| tornado_http             | 94.6 ms                                                    | 96.5 ms: 1.02x slower                                                    |
| regex_effbot             | 3.67 ms                                                    | 3.75 ms: 1.02x slower                                                    |
| pycparser                | 1.16 sec                                                   | 1.18 sec: 1.02x slower                                                   |
| dask                     | 369 ms                                                     | 378 ms: 1.02x slower                                                     |
| scimark_monte_carlo      | 69.2 ms                                                    | 70.8 ms: 1.02x slower                                                    |
| pickle                   | 11.5 us                                                    | 11.8 us: 1.02x slower                                                    |
| 2to3                     | 274 ms                                                     | 282 ms: 1.03x slower                                                     |
| coverage                 | 93.1 ms                                                    | 95.8 ms: 1.03x slower                                                    |
| python_startup           | 10.8 ms                                                    | 11.1 ms: 1.03x slower                                                    |
| bench_thread_pool        | 834 us                                                     | 859 us: 1.03x slower                                                     |
| sqlglot_normalize        | 110 ms                                                     | 114 ms: 1.03x slower                                                     |
| gunicorn                 | 1.28 ms                                                    | 1.32 ms: 1.03x slower                                                    |
| djangocms                | 31.5 us                                                    | 32.5 us: 1.03x slower                                                    |
| aiohttp                  | 1.18 ms                                                    | 1.22 ms: 1.03x slower                                                    |
| async_tree_none_tg       | 336 ms                                                     | 348 ms: 1.03x slower                                                     |
| telco                    | 8.41 ms                                                    | 8.71 ms: 1.04x slower                                                    |
| async_generators         | 442 ms                                                     | 458 ms: 1.04x slower                                                     |
| docutils                 | 2.83 sec                                                   | 2.94 sec: 1.04x slower                                                   |
| sympy_str                | 282 ms                                                     | 294 ms: 1.04x slower                                                     |
| chaos                    | 61.3 ms                                                    | 64.1 ms: 1.04x slower                                                    |
| json                     | 5.31 ms                                                    | 5.54 ms: 1.04x slower                                                    |
| sqlglot_optimize         | 55.5 ms                                                    | 58.0 ms: 1.04x slower                                                    |
| genshi_text              | 23.7 ms                                                    | 24.8 ms: 1.05x slower                                                    |
| nbody                    | 88.3 ms                                                    | 92.4 ms: 1.05x slower                                                    |
| sympy_expand             | 473 ms                                                     | 501 ms: 1.06x slower                                                     |
| dulwich_log              | 67.2 ms                                                    | 71.4 ms: 1.06x slower                                                    |
| django_template          | 34.8 ms                                                    | 37.1 ms: 1.07x slower                                                    |
| scimark_lu               | 122 ms                                                     | 130 ms: 1.07x slower                                                     |
| deltablue                | 3.25 ms                                                    | 3.48 ms: 1.07x slower                                                    |
| sympy_sum                | 156 ms                                                     | 167 ms: 1.07x slower                                                     |
| genshi_xml               | 51.6 ms                                                    | 55.7 ms: 1.08x slower                                                    |
| scimark_sor              | 127 ms                                                     | 138 ms: 1.08x slower                                                     |
| sympy_integrate          | 20.5 ms                                                    | 22.3 ms: 1.09x slower                                                    |
| regex_compile            | 137 ms                                                     | 149 ms: 1.09x slower                                                     |
| unpickle_pure_python     | 218 us                                                     | 238 us: 1.09x slower                                                     |
| mypy2                    | 742 ms                                                     | 812 ms: 1.09x slower                                                     |
| go                       | 145 ms                                                     | 158 ms: 1.09x slower                                                     |
| pathlib                  | 17.3 ms                                                    | 19.1 ms: 1.10x slower                                                    |
| raytrace                 | 267 ms                                                     | 296 ms: 1.11x slower                                                     |
| comprehensions           | 16.6 us                                                    | 18.5 us: 1.11x slower                                                    |
| nqueens                  | 81.4 ms                                                    | 93.5 ms: 1.15x slower                                                    |
| hexiom                   | 6.30 ms                                                    | 7.33 ms: 1.16x slower                                                    |
| python_startup_no_site   | 7.11 ms                                                    | 9.51 ms: 1.34x slower                                                    |
| Geometric mean           | (ref)                                                      | 1.01x slower                                                             |

Benchmark hidden because not significant (17): pylint, xml_etree_parse, async_tree_memoization, async_tree_io, unpickle, sqlglot_parse, xml_etree_iterparse, pprint_pformat, json_dumps, asyncio_websockets, regex_dna, sqlglot_transpile, json_loads, async_tree_cpu_io_mixed, pprint_safe_repr, async_tree_memoization_tg, async_tree_cpu_io_mixed_tg
Ignored benchmarks (2) of results/bm-20240605-3.13.0b2-3a83b17/bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17.json: bpe_tokeniser, flaskblogging
Ignored benchmarks (1) of results/bm-20240402-3.13.0a5+-5a3dca4-JIT/bm-20240402-linux-x86_64-brandtbucher-stitch_exhausted-3.13.0a5+-5a3dca4.json: unpack_sequence

# HPT report

- Reliability score: 99.96% likely to be slow
- 90% likely to have a slowdown of 1.01x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.07x