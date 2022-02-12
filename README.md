# FFMEPG

FFmpeg is a multimedia framework, able to decode, encode, transcode, mux,
demux, stream, filter and play pretty much anything that humans and machines
have created. It supports the most obscure ancient formats up to the cutting
edge. No matter if they were designed by some standards committee, the
community or a corporation.

## Creating the 'free' tarball

1. Update the `Version` in the spec file.
2. Set the `Release` to 0 in the spec file.
3. Do a full build locally: `fedpkg mockbuild --with full_build`
4. Run `./ffmpeg_update_free_sources.sh results_ffmpeg/5.0/0.fc35/build.log`
   This will update the `ffmpeg_free_sources` file list.
5. Run `./ffmpeg_gen_free_tarball.sh` to create the tarball.
6. Set the `Release` to 1 in the spec file.
7. Do a scratch build.
