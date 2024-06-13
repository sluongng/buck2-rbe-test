# A list of available rules and their signatures can be found here: https://buck2.build/docs/api/rules/

http_archive(
    name = "bazel_rules_go",
    sha256 = "51dc53293afe317d2696d4d6433a4c33feedb7748a9e352072e2ec3c0dafd2c6",
    urls = [
        # "https://mirror.bazel.build/github.com/bazelbuild/rules_go/releases/download/v0.40.1/rules_go-v0.40.1.zip",
        "https://github.com/bazelbuild/rules_go/releases/download/v0.40.1/rules_go-v0.40.1.zip",
    ],
    sub_targets = [
        "/".join(["go/tools/builders", a])
        for a in [
            "ar.go",
            "asm.go",
            "builder.go",
            "cgo2.go",
            "compilepkg.go",
            "cover.go",
            "edit.go",
            "embedcfg.go",
            "env.go",
            "filter.go",
            "filter_buildid.go",
            "flags.go",
            "generate_nogo_main.go",
            "generate_test_main.go",
            "importcfg.go",
            "link.go",
            "pack.go",
            "read.go",
            "replicate.go",
            "stdlib.go",
            "stdliblist.go",
            "path_windows.go",
            "path.go",
        ]
    ],
    visibility = ["PUBLIC"],
)

genrule(
    name = "ar",
    out = "out.go",
    cmd = "cat $(location //:bazel_rules_go[go/tools/builders/ar.go]) > $OUT",
)
