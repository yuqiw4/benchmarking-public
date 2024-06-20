# Results vs. 3.13.0b2

- fork: brandtbucher
- ref: justin_align
- machine: linux-x86_64
- commit hash: 790b1f8
- commit date: 2024-03-30
- overall geometric mean: 1.02x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.01x slower
- Memory change: 1.06x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240330-linux-x86_64-brandtbucher-justin_align-3.13.0a5+-790b1f8 |
|----------------|:----------------------------------------------------------:|:--------------------------------------------------------------------:|
| 2to3           | 274 ms                                                     | 281 ms: 1.02x slower                                                 |
| docutils       | 2.83 sec                                                   | 2.91 sec: 1.03x slower                                               |
| html5lib       | 67.2 ms                                                    | 66.7 ms: 1.01x faster                                                |
| tornado_http   | 94.6 ms                                                    | 97.5 ms: 1.03x slower                                                |
| Geometric mean | (ref)                                                      | 1.02x slower                                                         |

Benchmark hidden because not significant (1): chameleon

Benchmarks with tag 'asyncio':
==============================

| Benchmark          | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240330-linux-x86_64-brandtbucher-justin_align-3.13.0a5+-790b1f8 |
|--------------------|:----------------------------------------------------------:|:--------------------------------------------------------------------:|
| async_tree_none_tg | 336 ms                                                     | 345 ms: 1.03x slower                                                 |
| async_tree_none    | 378 ms                                                     | 394 ms: 1.04x slower                                                 |
| Geometric mean     | (ref)                                                      | 1.01x slower                                                         |

Benchmark hidden because not significant (6): async_tree_io_tg, async_tree_cpu_io_mixed, async_tree_cpu_io_mixed_tg, async_tree_memoization, async_tree_io, async_tree_memoization_tg

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240330-linux-x86_64-brandtbucher-justin_align-3.13.0a5+-790b1f8 |
|----------------|:----------------------------------------------------------:|:--------------------------------------------------------------------:|
| pidigits       | 191 ms                                                     | 189 ms: 1.01x faster                                                 |
| float          | 78.9 ms                                                    | 78.4 ms: 1.01x faster                                                |
| nbody          | 88.3 ms                                                    | 93.6 ms: 1.06x slower                                                |
| Geometric mean | (ref)                                                      | 1.01x slower                                                         |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240330-linux-x86_64-brandtbucher-justin_align-3.13.0a5+-790b1f8 |
|----------------|:----------------------------------------------------------:|:--------------------------------------------------------------------:|
| regex_dna      | 221 ms                                                     | 224 ms: 1.01x slower                                                 |
| regex_effbot   | 3.67 ms                                                    | 3.82 ms: 1.04x slower                                                |
| regex_compile  | 137 ms                                                     | 153 ms: 1.12x slower                                                 |
| Geometric mean | (ref)                                                      | 1.04x slower                                                         |

Benchmark hidden because not significant (1): regex_v8

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240330-linux-x86_64-brandtbucher-justin_align-3.13.0a5+-790b1f8 |
|----------------------|:----------------------------------------------------------:|:--------------------------------------------------------------------:|
| pickle_list          | 5.11 us                                                    | 4.96 us: 1.03x faster                                                |
| unpickle_list        | 5.34 us                                                    | 5.21 us: 1.03x faster                                                |
| pickle_dict          | 34.8 us                                                    | 34.1 us: 1.02x faster                                                |
| xml_etree_process    | 61.2 ms                                                    | 60.6 ms: 1.01x faster                                                |
| json_loads           | 28.9 us                                                    | 28.7 us: 1.01x faster                                                |
| pickle_pure_python   | 305 us                                                     | 306 us: 1.00x slower                                                 |
| xml_etree_generate   | 87.4 ms                                                    | 88.0 ms: 1.01x slower                                                |
| tomli_loads          | 2.12 sec                                                   | 2.18 sec: 1.03x slower                                               |
| pickle               | 11.5 us                                                    | 11.8 us: 1.03x slower                                                |
| unpickle_pure_python | 218 us                                                     | 251 us: 1.15x slower                                                 |
| Geometric mean       | (ref)                                                      | 1.01x slower                                                         |

Benchmark hidden because not significant (4): xml_etree_parse, unpickle, json_dumps, xml_etree_iterparse

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240330-linux-x86_64-brandtbucher-justin_align-3.13.0a5+-790b1f8 |
|------------------------|:----------------------------------------------------------:|:--------------------------------------------------------------------:|
| python_startup         | 10.8 ms                                                    | 11.1 ms: 1.03x slower                                                |
| python_startup_no_site | 7.11 ms                                                    | 9.51 ms: 1.34x slower                                                |
| Geometric mean         | (ref)                                                      | 1.17x slower                                                         |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240330-linux-x86_64-brandtbucher-justin_align-3.13.0a5+-790b1f8 |
|-----------------|:----------------------------------------------------------:|:--------------------------------------------------------------------:|
| mako            | 11.2 ms                                                    | 11.4 ms: 1.01x slower                                                |
| django_template | 34.8 ms                                                    | 36.1 ms: 1.04x slower                                                |
| genshi_text     | 23.7 ms                                                    | 25.0 ms: 1.06x slower                                                |
| genshi_xml      | 51.6 ms                                                    | 55.4 ms: 1.07x slower                                                |
| Geometric mean  | (ref)                                                      | 1.05x slower                                                         |

All benchmarks:
===============

| Benchmark                | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240330-linux-x86_64-brandtbucher-justin_align-3.13.0a5+-790b1f8 |
|--------------------------|:----------------------------------------------------------:|:--------------------------------------------------------------------:|
| typing_runtime_protocols | 165 us                                                     | 114 us: 1.45x faster                                                 |
| scimark_fft              | 392 ms                                                     | 357 ms: 1.10x faster                                                 |
| create_gc_cycles         | 1.82 ms                                                    | 1.66 ms: 1.09x faster                                                |
| gc_traversal             | 3.98 ms                                                    | 3.71 ms: 1.07x faster                                                |
| pylint                   | 317 ms                                                     | 300 ms: 1.06x faster                                                 |
| logging_silent           | 105 ns                                                     | 99.6 ns: 1.05x faster                                                |
| richards_super           | 57.4 ms                                                    | 54.6 ms: 1.05x faster                                                |
| sqlite_synth             | 2.99 us                                                    | 2.85 us: 1.05x faster                                                |
| mdp                      | 2.79 sec                                                   | 2.66 sec: 1.05x faster                                               |
| richards                 | 50.9 ms                                                    | 48.7 ms: 1.05x faster                                                |
| deepcopy_reduce          | 3.35 us                                                    | 3.23 us: 1.04x faster                                                |
| scimark_sparse_mat_mult  | 5.27 ms                                                    | 5.09 ms: 1.04x faster                                                |
| pickle_list              | 5.11 us                                                    | 4.96 us: 1.03x faster                                                |
| coroutines               | 23.2 ms                                                    | 22.5 ms: 1.03x faster                                                |
| unpickle_list            | 5.34 us                                                    | 5.21 us: 1.03x faster                                                |
| pickle_dict              | 34.8 us                                                    | 34.1 us: 1.02x faster                                                |
| deepcopy                 | 367 us                                                     | 364 us: 1.01x faster                                                 |
| pidigits                 | 191 ms                                                     | 189 ms: 1.01x faster                                                 |
| xml_etree_process        | 61.2 ms                                                    | 60.6 ms: 1.01x faster                                                |
| html5lib                 | 67.2 ms                                                    | 66.7 ms: 1.01x faster                                                |
| json_loads               | 28.9 us                                                    | 28.7 us: 1.01x faster                                                |
| float                    | 78.9 ms                                                    | 78.4 ms: 1.01x faster                                                |
| pickle_pure_python       | 305 us                                                     | 306 us: 1.00x slower                                                 |
| asyncio_tcp              | 508 ms                                                     | 510 ms: 1.00x slower                                                 |
| asyncio_websockets       | 567 ms                                                     | 570 ms: 1.01x slower                                                 |
| asyncio_tcp_ssl          | 1.84 sec                                                   | 1.85 sec: 1.01x slower                                               |
| bench_mp_pool            | 23.9 ms                                                    | 24.0 ms: 1.01x slower                                                |
| deepcopy_memo            | 39.7 us                                                    | 40.0 us: 1.01x slower                                                |
| xml_etree_generate       | 87.4 ms                                                    | 88.0 ms: 1.01x slower                                                |
| json                     | 5.31 ms                                                    | 5.36 ms: 1.01x slower                                                |
| sqlglot_parse            | 1.32 ms                                                    | 1.33 ms: 1.01x slower                                                |
| mako                     | 11.2 ms                                                    | 11.4 ms: 1.01x slower                                                |
| logging_format           | 6.47 us                                                    | 6.55 us: 1.01x slower                                                |
| regex_dna                | 221 ms                                                     | 224 ms: 1.01x slower                                                 |
| sqlglot_transpile        | 1.63 ms                                                    | 1.66 ms: 1.01x slower                                                |
| generators               | 29.6 ms                                                    | 30.1 ms: 1.02x slower                                                |
| meteor_contest           | 110 ms                                                     | 112 ms: 1.02x slower                                                 |
| dask                     | 369 ms                                                     | 377 ms: 1.02x slower                                                 |
| fannkuch                 | 402 ms                                                     | 411 ms: 1.02x slower                                                 |
| pycparser                | 1.16 sec                                                   | 1.18 sec: 1.02x slower                                               |
| 2to3                     | 274 ms                                                     | 281 ms: 1.02x slower                                                 |
| tomli_loads              | 2.12 sec                                                   | 2.18 sec: 1.03x slower                                               |
| async_tree_none_tg       | 336 ms                                                     | 345 ms: 1.03x slower                                                 |
| sqlglot_normalize        | 110 ms                                                     | 113 ms: 1.03x slower                                                 |
| bench_thread_pool        | 834 us                                                     | 857 us: 1.03x slower                                                 |
| docutils                 | 2.83 sec                                                   | 2.91 sec: 1.03x slower                                               |
| tornado_http             | 94.6 ms                                                    | 97.5 ms: 1.03x slower                                                |
| python_startup           | 10.8 ms                                                    | 11.1 ms: 1.03x slower                                                |
| aiohttp                  | 1.18 ms                                                    | 1.22 ms: 1.03x slower                                                |
| telco                    | 8.41 ms                                                    | 8.68 ms: 1.03x slower                                                |
| pickle                   | 11.5 us                                                    | 11.8 us: 1.03x slower                                                |
| gunicorn                 | 1.28 ms                                                    | 1.32 ms: 1.03x slower                                                |
| pprint_pformat           | 1.56 sec                                                   | 1.61 sec: 1.04x slower                                               |
| django_template          | 34.8 ms                                                    | 36.1 ms: 1.04x slower                                                |
| regex_effbot             | 3.67 ms                                                    | 3.82 ms: 1.04x slower                                                |
| sympy_str                | 282 ms                                                     | 294 ms: 1.04x slower                                                 |
| logging_simple           | 5.74 us                                                    | 5.98 us: 1.04x slower                                                |
| sqlglot_optimize         | 55.5 ms                                                    | 57.8 ms: 1.04x slower                                                |
| spectral_norm            | 116 ms                                                     | 121 ms: 1.04x slower                                                 |
| pyflate                  | 484 ms                                                     | 505 ms: 1.04x slower                                                 |
| async_tree_none          | 378 ms                                                     | 394 ms: 1.04x slower                                                 |
| async_generators         | 442 ms                                                     | 462 ms: 1.05x slower                                                 |
| scimark_sor              | 127 ms                                                     | 134 ms: 1.05x slower                                                 |
| chaos                    | 61.3 ms                                                    | 64.4 ms: 1.05x slower                                                |
| coverage                 | 93.1 ms                                                    | 97.8 ms: 1.05x slower                                                |
| pprint_safe_repr         | 758 ms                                                     | 798 ms: 1.05x slower                                                 |
| sympy_expand             | 473 ms                                                     | 499 ms: 1.06x slower                                                 |
| genshi_text              | 23.7 ms                                                    | 25.0 ms: 1.06x slower                                                |
| scimark_monte_carlo      | 69.2 ms                                                    | 73.3 ms: 1.06x slower                                                |
| nbody                    | 88.3 ms                                                    | 93.6 ms: 1.06x slower                                                |
| dulwich_log              | 67.2 ms                                                    | 71.4 ms: 1.06x slower                                                |
| mypy2                    | 742 ms                                                     | 792 ms: 1.07x slower                                                 |
| sympy_sum                | 156 ms                                                     | 167 ms: 1.07x slower                                                 |
| sympy_integrate          | 20.5 ms                                                    | 21.9 ms: 1.07x slower                                                |
| genshi_xml               | 51.6 ms                                                    | 55.4 ms: 1.07x slower                                                |
| deltablue                | 3.25 ms                                                    | 3.50 ms: 1.08x slower                                                |
| go                       | 145 ms                                                     | 159 ms: 1.10x slower                                                 |
| scimark_lu               | 122 ms                                                     | 134 ms: 1.10x slower                                                 |
| pathlib                  | 17.3 ms                                                    | 19.2 ms: 1.11x slower                                                |
| raytrace                 | 267 ms                                                     | 296 ms: 1.11x slower                                                 |
| regex_compile            | 137 ms                                                     | 153 ms: 1.12x slower                                                 |
| nqueens                  | 81.4 ms                                                    | 93.4 ms: 1.15x slower                                                |
| unpickle_pure_python     | 218 us                                                     | 251 us: 1.15x slower                                                 |
| comprehensions           | 16.6 us                                                    | 19.3 us: 1.16x slower                                                |
| hexiom                   | 6.30 ms                                                    | 7.56 ms: 1.20x slower                                                |
| python_startup_no_site   | 7.11 ms                                                    | 9.51 ms: 1.34x slower                                                |
| Geometric mean           | (ref)                                                      | 1.02x slower                                                         |

Benchmark hidden because not significant (15): async_tree_io_tg, async_tree_cpu_io_mixed, xml_etree_parse, crypto_pyaes, async_tree_cpu_io_mixed_tg, async_tree_memoization, thrift, chameleon, regex_v8, unpickle, json_dumps, xml_etree_iterparse, djangocms, async_tree_io, async_tree_memoization_tg
Ignored benchmarks (2) of results/bm-20240605-3.13.0b2-3a83b17/bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17.json: bpe_tokeniser, flaskblogging
Ignored benchmarks (1) of results/bm-20240330-3.13.0a5+-790b1f8-JIT/bm-20240330-linux-x86_64-brandtbucher-justin_align-3.13.0a5+-790b1f8.json: unpack_sequence

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.02x
- 95% likely to have a slowdown of 1.02x
- 99% likely to have a slowdown of 1.01x

# Memory
- memory change: 1.06x